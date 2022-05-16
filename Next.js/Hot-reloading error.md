문제
> docker 사용 시 윈도우에서 reloading이 안 되는 문제

원인
> 윈도우 내부적인 polling 설정 문제인 듯하다.

<br>

해결 방안
> next.config.js 파일에 다음 코드 추가
```js
module.exports = {
  webpackDevMiddleware: (config) => {
    config.watchOptions = {
      poll: 1000,
      aggregateTimeout: 300,
    };
    return config;
  },
};
```
* react의 경우 dockerfile 및 docker-compose.yml 파일에 CHOKIDAR_USEPOLLING=true 환경변수 설정으로 해결되는 경우도 많다고 한다.

<br>
<br>

참고 https://jameschambers.co.uk/nextjs-hot-reload-docker-development / https://www.inflearn.com/questions/65535
