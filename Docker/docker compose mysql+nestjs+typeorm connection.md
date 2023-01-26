문제
> docker compose로 nestjs+typeorm+mysql 연결 시도 중 에러 발생

<br>

원인
> 1. db connection을 위한 environment 설정 값이 일치하지 않음 <br>
> 2. mysql volume이 남아있어서 수정 사항이 제대로 반영되지 않음.

<br>

해결
> 1. docker compose config 로 docker-compose.yml 파일에 작성된 env 값들(DB_NAME, MYSQL_ROOT_PASSWD 등)이 정확히 입력되었는지 확인 <br>
> 2. docker compose down -v 로 남아있는 불필요한 볼륨을 삭제한 후 docker compose up --build로 재빌드

<br>
<br>
