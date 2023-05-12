문제
> docker compose로 elasticsearch container를 띄우자 아래 에러로 http://localhost:9200/ 접근 불가 <br>
```received plaintext http traffic on an https channel, closing connection netty4httpchannel```

<br>

원인
> elasticsearch의 보안 설정으로 인해 https를 위한 ssl 인증서가 필요

<br>

해결
> 임시적으로 http를 이용할 수 있게끔 관련 옵션을 false로 변경 <br>
> elascticsearch를 로컬에 설치한 경우 설치 경로의 elasticsearch.yml 파일에서 아래 옵션 수정
```
xpack.security.enabled: false
xpack.security.enrollment.enabled: false
xpack.security.http.ssl: enabled: false
xpack.security.transport.ssl: enabled: false
```
> docker compose로 실행시키는 경우 container 설정에 아래 옵션 추가
```
 environment:
    - xpack.security.enabled=false
```

<br>
<br>

참고 https://stackoverflow.com/questions/71492404/elasticsearch-showing-received-plaintext-http-traffic-on-an-https-channel-in-con / https://velog.io/@colacan100/%EC%97%90%EB%9F%AC%ED%95%B4%EA%B2%B0-Received-plaintext-http-traffic-on-an-https-channel-closing-connection
