> typeorm querybuilder로 복잡한 where절 작성하는 방법
```js
createQueryBuilder("user")
    .where("user.registered = :registered", { registered: true })
    .andWhere(
        new Brackets((qb) => {
            qb.where("user.firstName = :firstName", {
                firstName: "Timber",
            }).orWhere("user.lastName = :lastName", { lastName: "Saw" })
        }),
    )
```
```
SELECT ... FROM users user WHERE user.registered = true AND (user.firstName = 'Timber' OR user.lastName = 'Saw')
```

<br>
<br>

참고 https://typeorm.io/select-query-builder#adding-where-expression
