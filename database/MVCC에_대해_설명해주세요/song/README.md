MVCC는 Multi Version Concurrency Controll 의 약자로 뜻 그대로 여러 버전을 이용해 동시성 문제를 해결하는 기술이다.

언두로그를 이용해 트랜잭션이 변경하기 전 데이터를 저장하고 이 데이터를 읽어 잠금 없는 일관된 읽기를 지원한다.
