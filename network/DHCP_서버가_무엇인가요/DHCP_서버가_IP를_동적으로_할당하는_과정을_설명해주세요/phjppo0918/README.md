IP 주소 할당 절차는 총 4단계를 거치게 됩니다.

처음에는 단말이 DHCP를 탐색합니다 (DHCP Discover)
동일 서브넷 안에서 브로드캐스팅을 진행하여 모든 단말에게 메세지를 송신합니다.

그 다음으로는 DHCP가 offer 메세지를 제공합니다 (DHCP offer)
DHCP서버의 IP 주소와, 단말에 새로 할당할 IP 주소 정보를 브로드캐스팅 합니다.

그 다음으로는 DHCP 서버에게 요청을 보냅니다. (DHCP request)
DHCP 서버 존재를 확인한 단말은 DHCP 서버에게 수신된 IP를 할당해달라는 요청을 보냅니다.
이때 DHCP 서버가 단일이 아닐 수 있기 때문에 요청 또한 브로드캐스팅으로 보냅니다.

그 다음으로는 DHCP 서버가 응답하는데 (DHCP Ack)
request 메시지 안에 server identifier에 기록한 ip 주소가 자신의 주소인지 확인 후, 클라이언트가 사용해야 하는 IP 주소와 추가적인 네트워크 구성 정보 등을 응답으로 제공합니다. 

# 참고
https://net0.tistory.com/8

