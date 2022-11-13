문제
> multer와 aws sdk를 이용해서 사진 업로드 기능 개발 중 에러 발생

<br>

에러
> this.client.send is not a function

<br>

원인
> 두 모듈의 버전 불일치

<br>

해결
> multer s3와 aws sdk의 버전을 둘 다 2.x로 맞춰서 해결

<br>

참고 https://github.com/anacronw/multer-s3/issues/169 / https://github.com/MoonJongHyeon1095/hanghae99week6/issues/12
