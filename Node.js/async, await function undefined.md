문제
> 아래와 같은 코드에서 async, await가 연쇄적으로 일어나며 변수에 undefinded가 할당되는 문제

```js
const functionA = async ()=> {
    const user = await db.find()
    return user
}
```

```js
const mainFunc = async ()=> {
    const user = await functionA()
    console.log("user:",user) // undefinded
}
```
<br>

원인
> functionA의 async에 걸려 그 뒤의 console.log()가 먼저 실행되어버림.

<br>

해결
> functionA를 new Promise()로 만들어 해당 로직이 끝나기 전까지 다음 코드가 실행되지 않도록 함.
```js
const functionA = async ()=> {
    return new Promise((resolve, reject) => {
      const user = await db.find()
      resolve(user)
    }
}
```
<br>
<br>

참고 https://velog.io/@coin46/%EB%B9%84%EB%8F%99%EA%B8%B0%EB%A5%BC-%EC%B2%98%EB%A6%AC%ED%95%98%EB%8A%94-%EC%BD%9C%EB%B0%B1-Promise-asyncawait
