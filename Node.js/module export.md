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

참고 https://inpa.tistory.com/entry/NODE-%F0%9F%93%9A-require-%E2%9A%94%EF%B8%8F-import-CommonJs%EC%99%80-ES6-%EC%B0%A8%EC%9D%B4-1
