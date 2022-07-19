문제
> map 안에서 await을 사용하려고 했는데 에러 발생

<br>

에러
> 'await' expression is only allowed within an async function

<br>

해결 
> .map(async (arg) => { await ...} <br>

<br>
<br>

참고 https://stackoverflow.com/questions/47709969/await-expression-is-only-allowed-within-an-async-function
