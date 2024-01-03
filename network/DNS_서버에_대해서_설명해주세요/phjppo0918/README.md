DNS는 Domain Name System의 약자로, 호스트 이름을 IP주소로 변환해주는 분산형 DB 시스템을 말합니다.
dns 서버는 트리 구조로 이루어져 있으며, 도메인 표기 시에는 낮은 단계부터 표현하여 최상위 도메인이 가장 뒤에 나타내는 식으로 표기합니다.

기본적으로 DNS가 동작하는 과정은
만약 www.naver.com을 입력한다고 가정했을 때,
일단 Local Dns 서버에게 질의를 합니다.
만약 local dns 서버에 없으면 local dns 서버가 root dns 서버에게 질의를 합니다
root dns 서버에서 www.naver.com이 캐시되어있지 않으면
com 네임 서버의 ip 주소를 알려줍니다.
local dns 서버는 com dns서버에게 질의하여 www.naver.com의 ip 주소를 질의하고, naver.com의 네임 서버 주소를 받습니다.
이후, local dns 서버는 naver.com 네임서버에게 ip 주소를 질의하여 www.naver.com의 ip 주소를 받습니다.

# 참고
https://velog.io/@eunnbi/DNS와-작동-원리