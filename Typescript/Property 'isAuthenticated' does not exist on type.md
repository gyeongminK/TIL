문제
> passport 모듈을 사용하면서 req.isAuthenticated()를 사용하려 했으나 Property 'isAuthenticated' does not exist on type 에러 발생

<br>

원인
> typescript 에서 passport 모듈을 사용할 때 설정해줘야 할 것을 하지 않은 게 원인인 듯하다.

<br>

해결
> @types/passport 설치 후 Cannot invoke an object which is possibly 'undefined' 에러가 발생해 req.isAuthenticated?.()  
변경

<br>
<br>
 
 참고 https://stackoverflow.com/questions/56913963/cannot-invoke-an-object-which-is-possibly-undefined-ts2722
