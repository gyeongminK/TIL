문제
> 간헐적으로 DB에 동일한 유저 데이터가 두 개 쌓이는 문제 발생

<br>

원인
> Node.js는 기본으로 default timeout을 설정하기 때문에 req에 시간이 너무 오래 걸릴 경우 요청을 반복해 해당 에러가 발생할 수 있음.

<br>

해결
> ```req.connection.timeout(60*10*1000)``` 을 추가


<br>
<br>

참고 https://github.com/expressjs/express/issues/2512 / https://stackoverflow.com/questions/13150277/express-request-is-called-twice
