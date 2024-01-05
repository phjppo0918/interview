HTTP 1.1 버전은 Connection당 하나의 요청을 처리할 수 있으며, TCP 안에 2개 이상의 HTTP 요청을 담는 방식을 사용합니다.

이러한 방식은 앞선 요청에 의해 뒤의 요청까지 지연되는 HOL Blocking을 발생시킵니다.

또한, 불필요한 헤더 정보를 중복하여 계속 보내게 되어 불필요한 데이터를 주고받는데 네트워크 자원을 소비하는 문제가 발생합니다.


따라서 HTTP 2.0 버전에서는 기존 HTTP 1.1을 개선하였습니다.

먼저, Connection당 여러 개의 메시지를 주고받을 수 있도록 하고, 응답은 요청 순서와 상관없이 Stream으로 받아 HOL Blocking 문제를 해결하였습니다.

또한, 서버와 클라이언트는 Header table을 관리하여 이전 요청과 동일한 필드는 해당 테이블의 인덱스만 전송하는 방식으로 Header의 크기를 경량화 하였습니다.

- 참고
  - https://ssungkang.tistory.com/entry/%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC-HTTP-11-VS-HTTP-20