문제
> npm run start로 실행시켰을 때 제대로 import되어있는 모듈에 대해 Cannot find module 에러가 남.

<br>

원인
> 에러가 발생하는 곳을 확인하니 dist/ 였음 -> dist 폴더 구조가 꼬여서 발생

<br>

해결
> dist 폴더 구조를 외부 구조와 동일하게 맞춰주어서 해결 <br>
> 아예 dist 폴더 삭제 후 재실행해서 정돈된 상태의 dist가 다시 생성되게 하는 방법도 있다고 함.

<br>
