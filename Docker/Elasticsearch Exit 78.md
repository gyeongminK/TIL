에러
> Elasticsearch Container Stopped with Exit 78

<br>

원인
> max virtual memory areas (vm.max_map_count [65530])가 모자라서 생긴 에러

<br>

해결법
> sudo sysctl -w vm.max_map_count=262144

<br>
<br>
<br>

참고 https://github.com/laradock/laradock/issues/1699
