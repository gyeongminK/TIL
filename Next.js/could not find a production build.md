에러
> docker - next.js 세팅 과정에서 'could not find a production build in the '/app/.next' directory.' 에러 발생

원인
> 빌드 먼저 해야되는 문제 때문

해결법
> 도커파일 <br>
> RUN npm run build
> CMD ["npm", "run", "dev"] <br> 로 수정 
