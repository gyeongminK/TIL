문제
> sequelize-auto를 이용해 id가 존재하지 않는 기존 테이블을 뽑아 사용하려고 하니 해당 에러 발생

<br>

에러
> sequelizedatabaseerror: unknown column 'id' in 'field list'

<br>

원인
> sequelize는 primary key가 따로 정의되어있지 않으면 자동으로 id 칼럼을 추가하는데, 실제 테이블에는 id 칼럼이 존재하지 않아 발생한 에러

<br>

해결
> 다른 칼럼에 primaryKey: true 속성을 부여해 해결


<br>
<br>

참고 https://velog.io/@usaindream/Sequelize-%ED%8A%9C%ED%86%A0%EB%A6%AC%EC%96%BC4%ED%85%8C%EC%9D%B4%EB%B8%94-%EC%83%9D%EC%84%B1
