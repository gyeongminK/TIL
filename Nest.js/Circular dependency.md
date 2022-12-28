문제
> gateway와 service에서 서로를 inject 하자 오류 발생

<br>

해결
> `@Inject(forwardRef(() => CommonService))` 데코레이터 사용
```js
export class TestGateway implements OnGatewayConnection, OnGatewayDisconnect {
    constructor(
        @Inject(forwardRef(() => TestService))
        private testService: TestService,
    ) {}
```
```js
export class TestService {
    constructor(
        @Inject(forwardRef(() => TestGateway))
        private testGateway: TestGateway,
    ) {}
```


<br>
<br>

참고 https://stackoverflow.com/questions/68809112/inject-a-gateway-and-a-service-together-to-each-other-circular-dependency <br>
공식문서 https://docs.nestjs.com/fundamentals/circular-dependency
