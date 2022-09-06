문제
> ec2 상에서 docker-compose로 컨테이너들을 띄우는데 엘라스틱서치 137 exit 오류가 뜸

<br>

트러블 슈팅 과정
> 1. docker stats 로 메모리 상황을 확인
> 2. 메모리 limit이 750mb으로 설정되어있는 걸 확인
> 3. docker-compose.yml 파일에서 해당 컨테이너의 limit 설정 변경
```
  elasticsearch:
  . . .
    deploy:
      resources:
        limits:
          memory: 4g
```
> 4. 4기가로 늘어나지 않고 967메가 정도로만 늘어남 -> docker info로 도커 자체에게 설정되어있는 limit이 있는지 확인
> 5. linux의 경우 도커 자체의 limit은 없고 해당 컴퓨터의 메모리를 따라간다는 걸 알게 됨
> 6. ec2 인스턴스가 t1.micro인 탓에 애초에 최대 1기가까지밖에 할당될 수 없었음.(1기가 넘게 메모리를 사용하던 엘라스틱서치만 exit 오류가 나던 것)
> 7. 엘라스틱서치만 별개의 인스턴스로 분리하여 문제 해결


<br>
<br>

참고 https://stackoverflow.com/questions/44533319/how-to-assign-more-memory-to-docker-container / https://github.com/moby/moby/issues/22211 / https://www.baeldung.com/ops/docker-memory-limit / http://daplus.net/docker-docker-compose-%EB%B2%84%EC%A0%84-3%EC%97%90%EC%84%9C-%EB%A9%94%EB%AA%A8%EB%A6%AC-%EB%B0%8F-cpu-%EC%A0%9C%ED%95%9C%EC%9D%84-%EC%A7%80%EC%A0%95%ED%95%98%EB%8A%94-%EB%B0%A9%EB%B2%95/ 
