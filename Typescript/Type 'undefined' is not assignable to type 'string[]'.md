문제
> const spacings: Array<string> = req.user?._source?.scraps.spacing; <br>
> 위 코드에서 Type 'undefined' is not assignable to type 'string[]'. 에러 발생

<br>

원인
> 타입스크립트에서 null 값이 될 수 있는 값은 string[] 타입에 할당될 수 없다고 하는 에러

<br>

해결
> const spacings: Array<string> = req.user?._source?.scraps.spacing!; <br>
> 맨 뒤에 ! 를 붙여서 null 값이 오지 않는다고 알려줄 것
  
<br>
  <br>
  
  참고 https://stackoverflow.com/questions/54496398/typescript-type-string-undefined-is-not-assignable-to-type-string
