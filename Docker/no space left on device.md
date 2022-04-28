원인
- Docker에서 미리 할당된 용량이 이미 존재하는데, 이를 초과하는 경우 이 에러가 발생


<br> 

해결법

1) docker volume prune
> 볼륨 지우기

2) docker system prune 
> 사용 중인지 않은 컨테이너 모두 삭제
