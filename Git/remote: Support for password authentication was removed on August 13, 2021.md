문제
> git clone을 시도했는데 권한 오류 발생

<br>

에러
> remote: Support for password authentication was removed on August 13, 2021

<br>

원인
> 더이상 username, password로 권한 인증X, 개인 access token을 이용해야 함.

<br>

해결
> settings -> developer settings 들어가서 access token 발급받고 password 대신 해당 토큰 입력


<br>
<br>

참고 https://miracleground.tistory.com/entry/GitHub-토큰-인증-로그인-하기-오류-해결-remote-Support-for-password-authentication-was-removed-on-August-13-2021-Please-use-a-personal-access-token-instead / https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token
