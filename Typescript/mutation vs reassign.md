mutation
> updates the values present in the memory

<br>

reassign
> variable points to new memory locations where new values are stored

<br>

const vs let
> const: mutation(O), reassign(X) <br>
> let: mutation(O), reassign(O)

<br> 

* const로 선언한 배열, 객체의 뮤테이션 예시

```js
const foo = [];
foo.push("Apple");
foo.push("Orange");
```
```js
const event = new Date('August 19, 1975 23:15:30');
event.setDate(24);
```
<br>
<br>

참고 https://stackoverflow.com/questions/46553062/what-is-the-preferred-declaration-convention-for-objects-or-arrays-const-or-let / https://dev.to/jmitchell38488/const-let-var-javascript-variables-and-immutability-13ci / https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/setDate
