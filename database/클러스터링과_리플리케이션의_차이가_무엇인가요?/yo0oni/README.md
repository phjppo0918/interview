클러스터링
- DB를 여러 개의 서버가 나눠서 처리하도록 하는 것
- DB 서버를 하나로 두다가 이 서버가 죽으면 망하기 때문
- 여러 데이터베이스 서버로 만들면 부하를 분산시켜 사용자의 요청을 더 많이 수용할 수 있다. == 로드밸런싱
- 단, 병목현상이 발생할 수 있으며, 서버 운용 비용이 많이 든다.
- 수평적인 구조
- 여러 노드들 간의 데이터를 동기화하는 시간이 필요하므로 Replication에 비해 쓰기 성능이 떨어진다.


리플리케이션
- 마스터 DB에는 데이터의 수정사항을 반영만 하고, 리플리케이션을 하여 슬레이브 DB에 실제 데이터를 복사하는 것
- Master DB 역할 : 웹 서버로부터 데이터 등록, 수정, 삭제 요청시 로그를 생성하여 Slave DB로 전달
- Slave DB 역할 : Master DB로부터 받은 로그를 데이터로 반영
- 수직적인 구조
- 노드들 간의 데이터가 동기화되지 않아 일관성있는 데이터를 얻지 못할 수 있다.
