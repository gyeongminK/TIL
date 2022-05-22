문제
> req property 'nickname' does not exist on type 'User'.

<br>

원인
> @types/passport 에서 Request의 user(req.user)에 어떤 property가 들어갈 지를 알려주는 interface를 이미 정의해놓아서 생긴 오류

<br>

해결
> passport/index.ts 상단에 코드 추가 
```ts
declare global {
  // eslint-disable-next-line @typescript-eslint/no-namespace
  namespace Express {
    interface User {
      email: number;
      nickname: string;
      password: string;
    }
  }
}
 ```
<br>
<br>

참고 https://jeonghoj.github.io/2020/typescript-passport-req.user/
