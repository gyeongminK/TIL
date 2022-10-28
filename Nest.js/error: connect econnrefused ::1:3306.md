문제
> app.module에서  TypeOrmModule.forRoot로 디비 커넥션 설정을 해줬는데 해당 에러 발생

<br>

원인
> process.env에서 값을 가져오고 있던 것들이 undefined였음.

<br>

해결
> @nestjs/config 를 설치한 후 imports 리스트에 아래 코드를 넣어 해결
```ts
ConfigModule.forRoot({
          isGlobal: true,
          envFilePath: '.env'
        }),
```

<br>
<br>

참고 https://stackoverflow.com/questions/67116793/process-env-varible-undefined-in-nest-js
