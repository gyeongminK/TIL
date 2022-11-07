에러
> TypeError: (0 , twilio_1.default) is not a function

<br>

원인
> 해당 모듈의 import 방식이 잘못되었음

<br>

해결
> import twilio from 'twilio' 에서 import * as twilio from 'twilio'로 수정

<br>
<br>

참고 https://stackoverflow.com/questions/71865726/typeerror-0-dayjs-1-default-is-not-a-function
