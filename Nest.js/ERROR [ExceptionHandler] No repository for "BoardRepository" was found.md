문제
> ERROR [ExceptionHandler] No repository for "BoardRepository" was found. 에러 발생

<br>

원인
> typeorm과 @nestjs/typeorm 버전 문제

<br>

해결
> "typeorm": "^0.2.45", "@nestjs/typeorm": "^8.0.1" 으로 다운그레이드

<br>
<br>

참고 https://www.inflearn.com/questions/566544
