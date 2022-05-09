에러
>TypeError: Failed to execute 'fetch' on 'Window': Request with GET/HEAD method cannot have body.

<br>

원인
> swagger에서는 get method에 req.body 값을 줄 수 없음

<br>

해결법 
> 1) Get with Query Param (Query URL이 다소 복잡) <br>
> 2) Post with JSON Body (조회인데 Post라 마음이 불편함) <br>
> 3) Get with JSON (기존 방식, Forced, Swagger 에서는 정상 동작하지 않음) <br>
> 4) Get with Path Param (리소스 Path에 해당하지 않는 경우 있음. 다른 오류도 발생 가능)

<br>
<br>
<br>

참고 https://github.com/cloud-barista/cb-tumblebug/issues/489
