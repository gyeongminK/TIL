문제
> vi로 새 파일을 만들고 :wq 명령어를 입력했으나 저장 에러 발생

<br>

원인
> vi 하고 뒤에 경로/파일명 으로 입력 시 자동으로 해당 경로에 새 파일이 생성되는 줄 알았으나 폴더는 미리 만들어져 있어야 함.

<br>

해결
> 경로에 해당되는 폴더를 만든 후 새 파일 생성 <br>
> 위 문제로 인해 발생한 에러가 아닐 시 보통 sudo로 해결하거나 저장 시 :w !sudo tee % > /dev/null 명령어로 해결이 가능하다고 한다.


<br>
<br>

참고 https://iamrealizer.tistory.com/47