## HTTPS 통신에 대해 설명해주세요

HTTPS는 Hypertext Transger Protocol Secure의 약자로 
컴퓨터 네트워크를 통한 보안 통신에 사용되며 인터넷에서 널리 사용됩니다.


HTTPS 프로토콜을 사용하기 위해서는 인증기관으로 부터 SSL 인증서를 발급받아야 합니다.

### SSL 인증서
클라이언트와 웹 서버 간의 통신을 제 3자가 보증해주는 전자 문서입니다.

### 동작 과정
데이터를 대칭키 방식으로 암복호화, 공개키 방식으로 대칭키 전달

1. 클라이언트가 서버 접속하여 handshaking 과정에서 서로 탐색
    1-1. 클라이언트가 서버에게 전송할 데이터
    1-2. 클라이언트에 대한 응답으로 전송할 데이터
    1-3. 클라이언트 인증 확인
    1-4. 서버 인증 확인
2. 데이터 전송
3. 연결 종료 및 session key 폐기

