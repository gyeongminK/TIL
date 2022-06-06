문제
> GET /api/spellings/count 로 요청을 보내는데 GET /api/spellings/{id}로 요청이 가는 상황

<br>

원인
> elasticsearch에서는 고유 id 값이 문자열로 지정돼서 {id}에 문자열이 들어가게 됨. <br>
> 따라서 'count'를 주소가 아닌 id 문자열로 인식해서 해당 api로 요청을 잘못 보내고 있었던 것

<br>

해결
> count api를 따로 두려면 /api/spellings/count/all 등과 같이 {id}와 구분될 수 있도록 지정 필요. <br>
> 또는 그냥 /api/spellings 에서 count 정보를 같이 보내야 함.
