문제
> express로 elasticsearch로 쿼리문을 날리는데 내림차순으로 sort가 되지 않음 <br>
> elasticsearch는 '_score' 로 정렬할 때만 기본으로 내림차순 정렬이고 그 외 필드는 기본 오름차순 정렬
```js
const result = await esClient.search({
            index: index,
            body: {
              _source: ["title", "hits"],
              size: "10",
              sort: sort_by,
              query: {
                match: {
                  type: "spelling",
                },
              },
            },
          });
```
> 위의 코드처럼 작성했을 때 오름차순 정렬은 정상적으로 되었지만 desc 옵션을 주었을 때 아래 에러가 발생했다. <br>
> No mapping found for [sort_by] in order to sort on 

<br>

원인
> 정렬 필드를 query string으로 받아 변수로 넣어주는 과정에서 문법상의 오류가 있었던 것 같다.

<br>

해결
> body 바깥에서 템플릿 리터럴을 이용해 sort 값 넘겨주기
```js
const result = await esClient.search({
            index: index,
            sort: [`${sort_by}:desc`],
            body: {
              _source: ["title", "hits"],
              size: "10",
              query: {
                match: {
                  type: "spelling",
                },
              },
            },
          });
```
<br>
<br>
<br>


참고 https://stackoverflow.com/questions/38746994/sorting-on-elastic-search-with-node-js
