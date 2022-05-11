문제
> jest has detected the following 1 open handle potentially keeping jest from exiting 에러 발생

<br>

해결
> script에서 --detectOpenHandles 옵션 제거 후 "jest --forceExit"로 변경
