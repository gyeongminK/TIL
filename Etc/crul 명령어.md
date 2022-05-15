문제
> curl -X POST http://localhost:3000/users -H "Content-Type: application/json" -d '{"name": "Dexter", "email": "dexter.haan@gmail.com"}'<br>
> 윈도우에서 해당 명령어 입력 시 에러 발생

<br>

해결 방안
> curl.exe -X POST http://localhost:3000/users -H "Content-Type: application/json" -d '{₩"name₩": ₩"Dexter₩", ₩"email₩": ₩"dexter.haan@gmail.com₩"}' <br>
> 방식으로 바꿔서 입력

<br>
<br>
<br>

참고 https://guseowhtjs.tistory.com/entry/cURL-%ED%98%B8%EC%B6%9C%EC%9D%84-%ED%86%B5%ED%95%B4-HTTP-%EC%9A%94%EC%B2%AD%EC%9D%84-%EC%82%AC%EC%9A%A9%ED%95%98%EC%97%AC-%ED%97%A4%EB%8D%94%EB%A5%BC-%EB%B3%B4%EB%82%B4%EB%8A%94-%EB%B0%A9%EB%B2%95%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9E%85%EB%8B%88%EA%B9%8C?category=1009236
