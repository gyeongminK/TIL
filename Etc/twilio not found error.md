문제
> twilio sms 서비스 이용 중 아래 코드에서 key 값이 정확한데도 not found error 발생

```js
await twilioClient.verify.v2
                .services('<key 값>')
                .verificationChecks.create({ to: <번호>, code: <코드> });
```

<br>

원인
> sms 발송 후 verfiy를 한 번 하고나면 해당 인스턴스에 대한 내역이 사라지게 됨. <br>
> 이때 다시 verify를 하면 발송된 sms가 없으므로 not found 에러가 발생한 것

