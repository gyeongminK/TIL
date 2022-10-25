문제
> 간헐적으로 DB에 동일한 유저 데이터가 두 개 쌓이는 문제 발생

<br>

원인
> Node.js는 기본으로 default timeout을 설정하기 때문에 req에 시간이 너무 오래 걸릴 경우 요청을 반복해 해당 에러가 발생할 수 있음.

<br>

해결
> 1. ```req.connection.timeout(60*10*1000)``` 을 추가
> 2. 전역적으로 timeout을 설정하고 싶을 시 app.js에서 아래와 같이 설정
```js
const server = app.listen(3000, function () {
    server.setTimeout( 3 * 60 * 1000 )
});
```


<br>
<br>

참고 https://github.com/expressjs/express/issues/2512 / https://stackoverflow.com/questions/13150277/express-request-is-called-twice / https://medium.com/sjk5766/node-express-api%EA%B0%80-%EB%91%90-%EB%B2%88-%ED%98%B8%EC%B6%9C%EB%90%98%EB%8A%94-%ED%98%84%EC%83%81-b11f98a064e
