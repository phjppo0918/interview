## HTTP1.1과 HTTP2의 특징에 대해 설명해주세요

![http1/2](./http1/2.png)

### HTTP1.1
connection 한 개당 하나의 요청을 처리하도록 설계됨

HOL(Head Of Line) 블로킹 발생

네트워크에서 같은 큐에 있는 패킷이 첫번째 패킷에 의해 지연될 때 발생한즌 성능 저하 현상

RTT(Round Trip Time) 증가
connection 하나에 요청 한개를 처리하는 특성 때문에 3-way handshake가 반복적으로 일어나므로 불필요한 RTT 증가와 네트워크 지연을 초래해 성능을 지연시킵니다.

무거운 Header 구조
매 요청보다 중복된 헤더 값을 전송하고 서버 도메인에 관련된 쿠키 정보도 헤더에 함께 포함되어 전송됩니다.



### HTTP2
http1의 프로토콜 성능에 초첨을 맞춰 수정한 버전입니다.

multiplexed strems로 connection 한개를 동시에 여러 개의 메시지를 주고 받을 수 있으며 응답은 순서에 상관없이 stream으로 주고받습니다.


리소스 간의 의존관계에 따른 우선순위를 설정해 리소스 로드 문제를 해결하였습니다.

헤더 정보를 HPACK 방식으로 압축하였습니다.

출처
https://velog.io/@wiostz98kr/HTTP1.1%EA%B3%BC-HTTP2.0%EC%9D%98-%EC%B0%A8%EC%9D%B4-e2v4x4t1