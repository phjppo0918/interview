n+1 문제는 한 엔티티를 조회 시 해당 엔티티랑 관련한 엔티티를 N번 조회하는 문제를 말합니다.

JPA에서 해결할 수 있는 방법은
1. 즉시 로딩 설정
2. fetch join 사용
3. BetchSize 설정
4. EntityGraph 사용

이 있습니다.