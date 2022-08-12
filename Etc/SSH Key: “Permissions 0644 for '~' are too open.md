문제
> pem key로 ssh 접근 중 에러 발생

<br>

원인
> pem key의 접근 권한이 지나치게 허용적이었던 것이 원인

<br>

해결
> chmod 400 (pem key)의 방식으로 권한 수정


<br>
<br>

참고 https://stackoverflow.com/questions/29933918/ssh-key-permissions-0644-for-id-rsa-pub-are-too-open-on-mac
