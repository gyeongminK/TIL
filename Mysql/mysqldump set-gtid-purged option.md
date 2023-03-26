문제
> mysql dump 파일을 이용해 새로운 데이터베이스에 데이터를 복제하는데 데이터 유실 발생

<br>

원인
> rds db dump 시 --set-gtid-purged=OFF 옵션을 사용하지 않아 발생한 문제

<br>

**GTID란?**
- Global Transaction Identifier로, mysql에서 부여하는 고유 트랜잭션 id
- master와 slave간 동일한 식별자를 가지지 않는 경우 master에 문제가 생겼을 경우 slave를 이용한 장애 조치, 계층적 복제, 특정 시점으로의 백업 복구 작업 등에 어려움을 겪게 됨
- 이를 방지하기 위해 각 노드간 트랜잭션 단위의 동일한 식별자를 가지도록 한 것

<br>

 **--set-gtid-purged 옵션이란?**
 - mysqldump 시 ```SET @@GLOBAL.GTID_PURGED``` 구문 추가 여부 결정
 - GTID를 사용하지 않는 데이터베이스에 dump 데이터를 덮어씌울 예정일 경우 --set-gtid-purged=OFF 옵션을 사용해야 함

<br>
<br>

참고 http://www.gurubee.net/lecture/4213 / https://guide.ncloud-docs.com/docs/database-database-5-4
