문제
> created_at 으로 desc 정렬을 했으나 정렬되지 않음

<br>

원인
> date format 설정이 잘못되어 있었다.

<br>

해결
>   created_at: {
    type: "date",
    format: "yyyy-MM-dd",
  },
