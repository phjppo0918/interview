
TCP는 연결 설정 과정에서 3 way handshake로, 연결 해제 과정에서는 4 way handshake로 동작합니다.

3 way handshake는 다음 과정으로 동작합니다.
Client -> Server : SYN
Server -> Client : SYN ACK
Client -> Server : ACK
이 과정을 통해 양쪽 모두 데이터 전송 준비가 되었다는 것을 보장하고, 상대편의 초기 순차 일련 번호를 알아 순차적으로 전송 할 수 있게 해줍니다.

4 way handshake는 다음 과정으로 동작합니다.

Client -> Server : FIN(+ACK)
Server -> Client : ACK
Server -> Client : FIN
Client -> Server : ACK

맨 마지막에는 클라이언트가 서버로부터 FIN을 수신하더라도  아직 받지 못한 데이터가 있을 수 있으므로 TIME_WAIT을 합니다. 서버는 클라이언트의 ACK를 받은 이후 소켓을 닫습니다.
클라이언트도 TIME_WAIT 시간이 끝나면 소켓을 닫습니다.

즉, 연결 과정과 종료 과정이 차이나는 이유는 Client가 데이터 전송을 마쳤어도 Server가 아직 보낼 데이터가 남을 수 있기 때문에 서버가 일단 FIN에 대한 ACK만 보내고, 그 이후에 데이터를 모두 전송한 후에 자신도 FIN을 보내기 때문에 차이가 있습니다.