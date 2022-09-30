에러
> Cannot create property 'Symbol(level)' on string 

<br>

원인
> winstonlogger.log()에서 argument를 하나만 넘겨줘서 발생

<br>

해결
> winstonlogger.log('error', 'The transaction failed.'); 와 같이 추가해서 해결

<br>
<br>

참고 https://github.com/winstonjs/winston/issues/1166
