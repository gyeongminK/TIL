문제
> module.exports 로 export 했을 때 "** is not a function" 에러 발생

<br>

원인
> typescript랑 javascript 문법이 다름

<br>

해결
> export {객체, 함수 등} <br>
> import * as 별칭 from "상대경로"

<br>
<br>

참고 https://velog.io/@jkzombie/Typescript-%EC%9D%B5%ED%9E%88%EA%B8%B0-lib
