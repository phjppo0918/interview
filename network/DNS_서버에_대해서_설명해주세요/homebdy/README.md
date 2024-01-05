DNS 서버는 도메인 이름과 IP 주소를 서로 변환하는 기능을 수행하는 시스템입니다.

예를 들어 사용자가 www.naver.com을 브라우저에 입력하면 PC에 저장된 Local DNS에게 "www.naver.com"이라는 hostname"에 대한 IP 주소를 요청합니다.

Local DNS에 해당 도메인의 IP주소가 있다면 바로 응답하고, 없다면 다른 DNS 서버들과 통신을 시작합니다.

먼저 Root DNS 서버에게 해당 주소의 IP 주소를 요청합니다.
Root DNS에서도 해당 주소에 대한 IP주소가 존재하지 않을 경우 com 도메인을 관리하는 최상위 도메인 서버에 해당 주소에 대한 IP 주소를 요청합니다.

최상위 도메인 서버에서도 해당 주소를 찾을 수 없을 경우 naver.com DNS 서버에게 IP주소를 받아옵니다.

이를 응답받은 Local DNS는 www.naver.com의 IP 주소를 캐싱해놓고, 이후 다시 요청이 들어올 경우 응답해줍니다.


- 참고
  - https://inpa.tistory.com/entry/WEB-🌐-DNS-개념-동작-완벽-이해-★-알기-쉽게-정리#dns_동작_순서