## TCP의 혼잡제어에 대해 설명해주세요


혼잡제어는 송신측의 데이터 전달과 네트워크의 데이터 처리 속도 차이를 해결하기 위한 기법


### 해결 방법
1. AIMD(Additive Increase / Multiplication DEcrease)
처음에 패킷을 하나씩 보내고 이것이 문제 없이 도착하면 window 크기(단위 시간 내에 보내는 패킷의 수)를 1개씩 증가시켜가며 전송하는 방법


2. Slow Start(느린 시작)
패킷을 하났기 보내면서 시작하고, 패킷이 문제 없이 도착하면 각각의 ACK 패킷마다 window sie를 1씩 늘려줍니다.
전송 속도가 지수 함수 꼴로 증가합니다.


3. Fast Retransmit(빠른 재저송)
패킷을 받는 쪽에서 먼저 도착해야할 패킷이 도착하지 않고 다음 패킷이 도착한 경우에도 ACK 패킷을 보내게 됩니다.


4. Fast Recovery(빠른 회복)
혼잡한 상태가 되면 window size를 1로 줄이지 않고 반으로 줄이고 선형 증가시키는 방법입니다.


출처
https://gyoogle.dev/blog/computer-science/network/%ED%9D%90%EB%A6%84%EC%A0%9C%EC%96%B4%20&%20%ED%98%BC%EC%9E%A1%EC%A0%9C%EC%96%B4.html