에러
> fcm messaging 기능 이용 중 registration-token-not-registered 에러 발생

<br>

원인
> 유저가 앱을 설치해 디비에 fcm token이 등록된 후 앱을 삭제하면서 유효하지 않은 토큰이 됨.

<br>

해결
> 유효하지 않은 토큰을 디비에서 삭제할 수 있도록 fcm message 발송 로직의 catch문에 registration-token-not-registered 에러 발생 시 해당 유저의 fcm token을 지워주는 로직 추가

<br>
<br>

참고 https://firebase.google.com/docs/cloud-messaging/send-message?hl=ko#admin
