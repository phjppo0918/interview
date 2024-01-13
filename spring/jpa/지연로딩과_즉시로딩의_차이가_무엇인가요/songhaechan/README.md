### 즉시로딩 (Eager Loading)

연관된 객체를 한꺼번에 모두 조회하는 Fetch Type을 뜻한다.

EntityManager의 find()를이용한 메서드의 경우 jpa내부적으로 join으로 최적화해 단건 쿼리가 생성된다.

하지만 직접 우리가 jpql을 작성하기도하고, data jpa의 쿼리메소드도 jpa가 jpql를 생성하는데

이때 jpql은 sql로 바로 번역되기때문에 join최적화가 불가능하다.

즉 N+1 문제가 발생하고, Eager의 경우 해결이 불가능하다.

## 지연 로딩(Lazt Loading)

연관된 객체를 바로 DB에 조회쿼리를 보내지않는다. 자바 객체를 조회하려는 순간 DB에 쿼리가 날아간다.
