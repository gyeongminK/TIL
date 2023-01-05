- typeorm querybuilder로 원하는 날짜 데이터 형식대로 groupBy해서 데이터 count 및 select 하기


```js
const dateList = await this.testRepository
            .createQueryBuilder('test')
            .select('DATE_FORMAT(test.createTime,"%d/%m/%Y %l%p") date')
            .addSelect('COUNT(*) as cnt')
            .where('test.id = :id', { id: id })
            .groupBy('date')
            .getRawMany();
```
<br>

- DATE_FORMAT() 형식 관련 자료 https://j07051.tistory.com/606
- COUNT()를 사용하지 않을 시 getMany()를 사용해야 함.
