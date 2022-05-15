문제
> module.exports 로 export 했을 때 "** is not a function" 에러 발생

<br>

원인
> commonjs와 ES6 문법의 차이

<br>

해결
1) commonjs
- module.exports = {};
- const 변수명 = require("");

<br>

2) ES6
- export {객체, 함수 등};
- import * as 별칭 from "";

<br>
<br>

참고 https://velog.io/@jkzombie/Typescript-%EC%9D%B5%ED%9E%88%EA%B8%B0-lib
