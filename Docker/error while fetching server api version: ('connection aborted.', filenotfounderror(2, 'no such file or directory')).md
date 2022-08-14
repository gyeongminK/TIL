문제
> ec2 내부에서 docker-compose up을 했을 때 에러 발생

<br>

애러
> error while fetching server api version: ('connection aborted.', filenotfounderror(2, 'no such file or directory'))

<br>

원인
> docker가 켜져 있지 않았음

<br>

해결
> systemctl status docker 로 도커 상태 확인 후 <br>
> systemctl start docker 실행 <br>
> 이때 아래와 같은 에러가 발생하면 sudo로 실행하면 됨.
```
failed to start docker.service: the name org.freedesktop.policykit1 was not provided by any .service files
```


<br>
<br>

참고 https://stackoverflow.com/questions/64952238/docker-errors-dockerexception-error-while-fetching-server-api-version
