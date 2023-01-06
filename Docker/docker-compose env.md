- docker-compose.yml 파일에서 .env 값 사용하는 방법 <br>
  - .env 
  ```MYSQL_ROOT_PASSWORD = 1234```
  - docker-compose.yml ```MYSQL_ROOT_PASSWORD: ${MYSQL_ROOT_PASSWORD}```

<br>

참고 https://docs.docker.com/compose/environment-variables/
