문제
> new Date()로 시간 설정 시 한국 시간으로 설정되지 않음

<br>

원인
> 한국 시간과 UTC(세계 협정시)의 시차 때문

<br>

해결
> new Date(+new Date() + 9 * 60 * 60 * 1000) <br>
> 9시간의 시차를 밀리초 단위로 변환해서 해결


<Br>
  <br>
  <Br>
    
참고 https://gurtn.tistory.com/65 / https://hianna.tistory.com/451
