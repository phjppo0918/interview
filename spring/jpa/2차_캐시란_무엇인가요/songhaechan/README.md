## JPA 2차 캐시

JPA의 1차 캐시(영속성 컨텍스트 그 자체)는 트랜잭션 커밋, Flush 시 종료되기때문에 획기적인 성능 향상을 얻기 힘들다.

애플리케이션이 죽기직전까지 메모리에 데이터를 유지하는 2차캐시(공유캐시)를 JPA는 지원하는데

1차캐시에 데이터가 없어도 DB에 직접 조회하지않고 2차캐시를 찾은 뒤에도 없다면 DB를 조회한다.

여러 스레드가 동시에 접근해 동시성 문제가 발생할 수 있기때문에 2차캐시의 데이터를 복사해서 1차캐시(영속성컨텍스트)에 반환한다.
