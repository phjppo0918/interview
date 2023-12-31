## TCP의 흐름제어에 대해 설명해주세요

흐름제어는 송신측과 수신측의 데이터 처리 속도 차이를 해결하기 위한 기법입니다.


수신측이 송신측보다 데이터 처리 속도가 빠르면 문제없지만, 송신측의 속도가 빠를 경우 문제가 발생합니다.


수신측에서 제한된 저장 용량을 초과한 이후에 도착하는 데이터는 손실 될 수 있으며, 만약 손실이 된다면 불필요하게 응답과 데이터 전송이 송/수신 측 간에 빈번히 발생합니다.


### 해결 방법

1. Stop and Wait
    매번 전송한 패킷에 대해 확인 응답을 받아야만 그 다음 패킷을 전송하는 방법
2. Sliding Window
    수신 측에서 설정한 윈도우 크기만큼 송신 측에서 확인 응답없이 세그먼트를 전송 할 수 있게 하여 데이터 흐름을 동적으로 조절하는 제어 기법



