문제
> npm i 시 npm ERR! ERESOLVE could not resolve Could not resolve dependency 에러 발생

<br>

원인
> npm 7버전부터는 peer dependency가 있을 시 설치가 막히게 됨.
> * peer dependency: 실제로 패키지에서 직접 require(import) 하지는 않더라도 호환성이 필요한 경우

<br>

해결
> --force 또는 --legacy-peer-deps 옵션 사용 <br>
> --force: package-lock.json에 몇가지의 다른 의존 버전들을 추가 <br>
> --legacy: peerDependency가 맞지 않아도 일단 설치

<br>
<br>

참고 https://velog.io/@yonyas/Fix-the-upstream-dependency-conflict-installing-NPM-packages-%EC%97%90%EB%9F%AC-%ED%95%B4%EA%B2%B0%EA%B8%B0 /
https://velog.io/@johnyworld/Peer-Dependencies-%EC%97%90-%EB%8C%80%ED%95%98%EC%97%AC
