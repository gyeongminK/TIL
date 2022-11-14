문제
> nest.js에서 middleware를 설정하던 중 에러 발생

<br>

에러
> Cannot set headers after they are sent to the client

<br>

원인
> 미들웨어 내부에서 next()가 여러 개 실행될 수 있는 환경이라 에러 발생

<br>

해결
> return next()로 한 번만 실행될 수 있게 수정

<br>
<br>

참고 https://stackoverflow.com/questions/72509784/nestjs-error-cannot-set-headers-after-they-are-sent-to-the-client
