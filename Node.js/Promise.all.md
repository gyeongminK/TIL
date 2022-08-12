문제
> async await을 이용해 비동기로 코드를 짜던 중 map 안에서의 async await이 끝나기 전 다음 await 코드가 실행되는 문제 발생

<br>

해결
> Promise.all 을 이용해 map 안에서의 await 과정을 병렬적으로 처리하고, 해당 구문이 끝나기 전 다음 await이 실행되지 않도록 함
