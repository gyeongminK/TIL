문제
> jsonwebtoken에서 import한 jwt의 decode type 때문에 에러 발생

<br>

에러
> property 'payload' does not exist on type 'string'.

<br>

해결
> import jwt from 'jsonwebtoken';를 <br>
> const jwt = require('jsonwebtoken'); 로 변경

<br>

참고 https://stackoverflow.com/questions/47508424/how-to-get-token-expiration-with-jsonwebtoken-using-typescript
