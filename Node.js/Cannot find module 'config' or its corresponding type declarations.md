문제
> config 폴더를 만들어줬는데 import * as config from 'config'; 에서 모듈을 찾지 못 함.

<Br>
  
에러
> Cannot find module 'config' or its corresponding type declarations.

<br>

원인
> config package 미설치 + typescript 버전 문제

<br>

해결
> npm i config + typescript@4.3.5 버전으로 업그레이드

<br>
<br>

참고 https://stackoverflow.com/questions/21599252/error-cannot-find-module-config
