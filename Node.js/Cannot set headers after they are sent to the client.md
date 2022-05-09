에러
> [ERR_HTTP_HEADERS_SENT]: Cannot set headers after they are sent to the client

<br>

원인
> 서버가 클라이언트에 둘 이상의 응답을 보내려고 할 때 발생

<br>

해결법
> if 조건부에서 전송되는 응답에 javascript return 문을 추가하여 응답이 클라이언트에 전송되면 코드 종료시키기

<br>
<br>

참고 https://velog.io/@yhe228/ERRHTTPHEADERSSENT-Cannot-set-headers-after-they-are-sent-to-the-client
