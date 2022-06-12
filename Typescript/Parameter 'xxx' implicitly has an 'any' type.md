문제
> new_scraps.some(item => item.id === req.params.id) 에서 Parameter 'item' implicitly has an 'any' type. 에러 발생

<br>

원인
> new_scraps의 타입을 알 수 없어서 생긴 에러.

<br>

해결
> new_scraps.some((item: any) => item.id === req.params.id)로 수정 <br>
> 또는 new_scraps의 타입을 따로 지정해줘야 함

<br>
<br>

참고 https://stackoverflow.com/questions/43064221/typescript-ts7006-parameter-xxx-implicitly-has-an-any-type
