에러
> illegal mix of collations (utf8mb4_0900_ai_ci,implicit) and (utf8mb4_general_ci,implicit) for operation '=’

<br>

원인
> join을 건 테이블의 char set과 collate이 다름

<br>

해결
> join하는 테이블들의 collate을 일치시켜줘서 해결

<br>
<br>

참고 https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=rorean&logNo=221528859835
