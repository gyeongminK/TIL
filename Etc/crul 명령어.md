문제
> curl -X POST http://localhost:3000/users -H "Content-Type: application/json" -d '{"name": "Dexter", "email": "dexter.haan@gmail.com"}'<br>
> 윈도우에서 해당 명령어 입력 시 에러 발생

<br>

해결 방안
> curl.exe -X POST http://localhost:3000/users -H "Content-Type: application/json" -d '{₩"name₩": ₩"Dexter₩", ₩"email₩": ₩"dexter.haan@gmail.com₩"}' <br>
> 방식으로 바꿔서 입력
