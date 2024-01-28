read uncommitted

복수의 트랜잭션들은 서로 커밋되지 않은 사항까지 select할 수 있어 데이터 무결성이 매우 떨어진다.

dirty read, non-repeatable read, phantom read 모두 발생한다.

dirty read는 다른 트랜잭션에서 변경하고 커밋하지 않은 사항을 읽게되는 문제점이다.

read committed

서로 커밋한 사항만 select할 수 있다.

dirty read는 발생하지 않지만 반복해서 읽을 수 없는 문제가 있다.

다른 트랜잭션이 커밋하면 dirty read는 아니지만 복수의 조회에서 서로 조회결과가 다르게 조회된다.

repeatable read

반복적인 조회에도 항상 같은 결과를 보장한다.

다른 트랜잭션이 변경을 가하면 언두로그에 변경 전 데이터를 기록하고 계속 같은 결과를 얻을 수 있다.

이런 변경방식을 MVCC라 한다.

보통 이 격리수준은 팬텀리드는 발생시키지만 MySQL은 갭락으로 문제를 해결해 발생하지않는다.

serializable

모든 트랜잭션은 순차적으로 수행된다. 성능에 굉장히 좋지 못하다.
