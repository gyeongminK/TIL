에러
> org.springframework.beans.factory.beancreationexception: error creating bean with name 'springdatajpamemberrepository'

<br>

원인
> 스프링 데이터 JPA에서는 메서드 이름이 규칙에 맞아야 함. findByID가 규칙에 맞지 않아 발생한 에러

<br>

해결
> findByID -> findById 로 수정


<br>
<br>

참고 https://www.inflearn.com/questions/128077
