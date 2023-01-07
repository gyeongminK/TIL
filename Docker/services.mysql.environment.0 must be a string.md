문제
> docker-compose.yml 파일에서 mysql 환경설정을 했는데 에러 발생

<br>

에러
> services.mysql.environment.0 must be a string

<br>

원인
> 아래와 같이 설정
```
  mysql:
    image: library/mysql:8.0
    container_name: mysql
    restart: always
    ports:
      - 3306:3306
    environment:
      - MYSQL_ROOT_PASSWORD: ${MYSQL_PASSWORD}
```

<br>

해결
- environment 설정 방식을 변경해서 해결
```
  mysql:
    image: library/mysql:8.0
    container_name: mysql
    restart: always
    ports:
      - 3306:3306
    environment:
      - MYSQL_ROOT_PASSWORD=${MYSQL_PASSWORD}
```

<br>
<br>

참고 https://stackoverflow.com/questions/50184525/docker-compose-throws-invalid-type-error
