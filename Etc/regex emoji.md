> 정규표현식으로 영문자, 숫자, 일부 특수문자, 이모지 허용하는 법


```
/^(?=.*[a-zA-Z\\d\s`~!@#$%^&*()-_=+])[a-zA-Z\\d\s`~!@#$%^&*()-_=+]|\P{L}+$/
```
<br>
<br>

참고 https://stackoverflow.com/questions/63744423/regex-to-match-english-special-characters-and-emojis
