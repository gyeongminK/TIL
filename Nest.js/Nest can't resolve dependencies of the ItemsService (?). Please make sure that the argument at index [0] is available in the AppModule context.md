애러
> Nest can't resolve dependencies of the ItemsService (?). Please make sure that the argument at index [0] is available in the AppModule context.

<br>

해결
> app.module.ts에서 다른 모듈에서 이미 import되어있는 service와 controller 삭제


<br>
<br>

참고 https://stackoverflow.com/questions/56870498/nest-cant-resolve-dependencies-of-the-itemsservice-please-make-sure-that-t
