문제
> typeorm으로 아래 예시와 같은 find 쿼리 사용 중 Unknown column 'distinctAlias' 에러 발생
```ts
const data = await this.repository.find({
    where: [
        {
            a: { id: tester1.id },
            createTime: LessThan(date),
        },
        {
            b: { id: tester2.id },
            createTime: LessThan(date),
        },
    ],
    relations: {
        a: true,
        b: true
    },
    select: {
        id: true,
        a: true
        createTime: true,
    },
    take: 50,
    order: {
        createTime: 'DESC',
    },
});
```

<br>

해결
> select문에 'id' 추가

<br>
<br>

참고 https://github.com/typeorm/typeorm/issues/4159
