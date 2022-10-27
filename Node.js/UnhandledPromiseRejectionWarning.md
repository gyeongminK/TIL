문제
> async await을 활용해 비동기 처리를 하는 과정에서 해당 에러 발생

<br>

에러
> UnhandledPromiseRejectionWarning: Unhandled promise rejection. This error originated either by throwing inside of an async function without a catch block, or by rejecting a promise which was not handled with .catch(). 


<br>

해결
> throw 하는 구문 바깥을 try catch문으로 감싸서 해결

<br>
<br>

참고 https://dev-dain.tistory.com/77
