문제
> postman에서 api 테스트를 하는 데 해당 에러 발생

<br>

에러
> Error: write EPROTO 34557064:error:100000f7:SSL routines:OPENSSL_internal:WRONG_VERSION_NUMBER

<br>

원인
> http만 지원하는 api에 https로 요청을 보냄

<br>

해결
> http로 주소 변경


<br>
<br>

참고 https://stackoverflow.com/questions/62658941/error-write-eproto-34557064error100000f7ssl-routinesopenssl-internalwrong

