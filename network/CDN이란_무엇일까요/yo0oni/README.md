CDN이란 콘텐츠 전송 네트워크(Content Delivery Network)로, 수많은 데이터를 다수 사용자들에게 동시에 전달할 때 사용하는 분산 서버이다.

단일 초대형 서버를 만들어 운용할 경우
단일 고장 지점,
네트워크 혼잡,
멀리 떨어진 클라이언트 처리 지연,
등 확장성 문제를 갖는다.

이러한 문제점을 극복하기 위한 것이 CDN이다. 대표적인 서비스로 넷플릭스와 유튜브가 있다.
CDN 동작 방식은, 여러개의 CDN 노드를 만들고, 그 노드에 데이터 복사본을 저장한다.
서비스 이용자는 해당 CDN 노드에 데이터 요청을 보낸다. 그러면 가입자 근처의 CDN이 데이터 복사본을 제공한다.

동작 방식은 다음과 같다.
1. 사용자가 원본 데이터를 갖고 있는 서버로 요청을 보내긴한다.
2. 그러면 해당 서버가 사용자에게 CDN 서버 주소를 알려준다.
3. 그럼 사용자는 다시 CDN 서버로 요청을 보낸다.
4. 해당 CDN 서버는 데이터 복사본을 갖고 있기 때문에, 해당 데이터를 사용자에게 전달한다.

동작 방식은 복잡하지만, 실제로는 사용자가 지연을 느끼지 못할 정도로 빠르게 처리된다.