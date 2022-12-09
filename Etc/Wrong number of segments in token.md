문제
> Google OAuth Api로 토큰을 verify하는 과정에서 에러 발생

<br>

에러
> Wrong number of segments in token

<br>

원인
> access token이 아닌 id token을 verify 해야 됐음.

<br>

해결
> 클라이언트로부터 id token을 받아 아래 코드를 통해 verify 성공 <br>
> 관련 레퍼런스 https://developers.google.com/identity/sign-in/web/backend-auth
```ts
const client = new OAuth2Client(process.env.GOOGLE_CLIENT_ID);
                const ticket = await client.verifyIdToken({
                    idToken: googleToken,
                    audience: process.env.GOOGLE_CLIENT_ID,
                });
                const payload = ticket.getPayload();
```

<br>
<br>
