문제
> ec2 상에서 도커를 사용하려고 했을 때 에러 발생

<br>

에러
> docker.errors.DockerException: Error while fetching server API version

<br>

원인
> docker가 정상 작동 중이지 않았음.

<br>

해결
> systemctl start docker


<br>
<br>

참고 https://stackoverflow.com/questions/64952238/docker-errors-dockerexception-error-while-fetching-server-api-version / https://stackoverflow.com/questions/64662372/docker-compose-up-error-while-fetching-server-api-version-connection-aborte
