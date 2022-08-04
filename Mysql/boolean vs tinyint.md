문제
> boolean으로 타입을 선언했으나 tinyint 타입으로 바뀜.

<br>

원인
> mysql에는 bool 타입이 없고 tinyint 타입이 있음.

<br>

설명
> boolean으로 타입을 설정하면 tinyint(1)로 자동 변환해 1비트의 메모리를 할당해 0 또는 1의 값을 가지도록 함. <br>
> 이때 true는 1로, false는 0으로 저장되게 됨.

<br>
<br>

참고 https://kkumalog.tistory.com/79
