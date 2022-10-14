에러
> AssertionError [ERR_ASSERTION]: Missing where attribute in the options parameter

<br>

원인
> update문에서 문법 오류

<br>

해결
> 아래와 같이 수정해 해결
```js
await User.update({
    name: name
  },
  {
    where: { email: email }
})
```


<br>
<br>

참고 https://jootc.com/p/202205143864
