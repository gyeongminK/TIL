에러
> Web server failed to start. Port 8080 was already in use.

<br>

원인
> 포트가 이미 실행 중일 때 스프링을 run 한 것

<br>

해결
> lsof -i tcp:8080 로 동작 중인 프로세스 확인 후 sudo kill -9 {PID}

<br>
<br>

참고 https://dundung.tistory.com/148
