문제
> user data를 multer로 넘기는 문제

<br>

해결
> res.locals를 이용해 해당 req가 유효한 동안 공통으로 유지되는 변수 전달 <br>


```js
router.get('/', userCheck, upload, controller)
```
```js
const upload = (req, res, next)=>{
  const userData = res.locals.userData
  return multer({
    storage: multerS3({
      s3: ~,
      bucket: ~,
      acl: ~,
      contentType: ~,
      metadata: (req, file, cb) => {
        cb(null, { fileName: file.fieldname })
      },
      key: (req, file, cb) => {
        cb(null, `${userData}/~`);
      }
    }),
  }).fields([{name:'file'}]);
}
```
<br>

