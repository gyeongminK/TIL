문제
> getMany()와 COUNT 쿼리를 동시에 사용할 수 없음.

<br>

원인
> COUNT 등과 같은 쿼리를 이용해 특징 데이터를 뽑아오고 싶은 경우 getRawMany()를 이용해야 함.<br>
> getMany()의 경우 전체 엔티티를 반환하기 때문에 특정 데이터만 뽑아오는 데에 적합하지 않음.

<br>

해결
> COUNT문과 getRawMany()를 이용해 해결

<br>
<br>

참고 https://github.com/typeorm/typeorm/issues/544 / https://stackoverflow.com/questions/70179506/typeorm-what-is-the-difference-between-getrawmany-and-getmany
