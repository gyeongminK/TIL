문제
> filter() 함수를 사용하는데 배열이 필터링되지 않는 문제 발생

<br>

원인
> filter() 내부에서 return을 해주지 않음. <br>
> 화살표 함수를 이용해 한 줄로 코드를 작성했을 시 return을 별도로 해주지 않아도 되지만, 그게 아닐 때에는 return을 해줘야 함.
```js
const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

console.log(result);
// output: Array ["exuberant", "destruction", "present"]

```

```js
const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => {
  word.length > 6
});

console.log(result);
// output: Array []
```
```js
const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => {
  return word.length > 6
});

console.log(result);
// output: Array ["exuberant", "destruction", "present"]
```

<br>
<br>

참고 https://debbie.codes/blog/js-array-filter-method/ / https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter
