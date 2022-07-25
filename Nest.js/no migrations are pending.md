문제
> migration:generate 후 migration:run 을 했는 데 스키마 변경 사항이 반영되지 않음.

<br>

원인
> synchronize가 false로 설정되어 있었음.

<br>

해결
> synchronize: true 로 변경
