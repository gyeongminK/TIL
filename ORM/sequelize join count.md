> sequelize로 join 테이블의 count 값 기준 쿼리 작성하기
```js
        const result = await tableA.findAll({
            include: [
                {
                    model: tableB,
                    as: 'tableB',
                    attributes: [],
                    where: {
                        deletedAt: {
                            [Op.ne]: null,
                        },
                    },
                },
            ],
            group: ['tableA.id'],
            having: Sequelize.where(Sequelize.fn('COUNT', Sequelize.col('tableB.id')), {
                [Op.gt]: 0,
            }),
            where: { creater: email },
        });
```
