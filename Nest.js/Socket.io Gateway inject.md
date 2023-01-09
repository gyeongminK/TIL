문제
> gateway를 다른 모듈의 service에서 사용하는데 connection이 두 개씩 생기는 문제 발생

<br>

원인
> 해당 모듈에서 아래와 같이 gateway 주입 <br>
> gateway 자체를 provider에 넣어서 gateway가 두 개로 작용함
```
@Module({
    imports: [
        TypeOrmModule.forFeature([
            User,
        ]),
    ],
    controllers: [TestController],
    providers: [TestService, ServerGateway],
})
export class TestModule {}
```

해결
> ServerModule에서 ServerGateway를 exports 해준 뒤 아래와 같이 변경
```
@Module({
    imports: [
        TypeOrmModule.forFeature([
            User,
        ]),
        ServerModule
    ],
    controllers: [TestController],
    providers: [TestService],
})
export class TestModule {}
```

<br>
