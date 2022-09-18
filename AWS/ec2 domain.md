문제
> ec2 domain 연결(route 53과 가비아 이용) 후 해당 주소로 접근이 불가능함.

<br>

에러
> err_connection_refused 

<br>

원인
> ec2의 기본 포트는 80번이기 때문에 80번 포트로 연결되어있지 않은 경우 주소 뒤에 :3000 등을 붙여 포트를 따로 명시해줘야 함.

<br>

해결
> sudo iptables -A PREROUTING -t nat -i eth0 -p tcp --dport 80 -j REDIRECT --to-port 3000 <br>
> 위 명령어로 80번 포트를 해당 웹 페이지의 기본 포트로 리다이렉트시켜서 해결

<br>
<br>

참고 https://happiestmemories.tistory.com/47
