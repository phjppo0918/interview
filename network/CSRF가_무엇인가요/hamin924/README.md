## CSRF가 무엇인가요?

Cross Site Request Forgery의 줄임말로 웹 취약점 중 하나입니다.

공격자가 희생자의 권한을 도용해 특정 웹 사이트의 기능을 실행 할 수 있습니다.

CSRF를 통해 공격을 하기 위해선 아래의 조건이 만족되어야 합니다.

​
희생자가 공격자가 만든 피싱 사이트에 접속할 것

희생자가 위조 요청을 보낼 사이트(상기한 페이스북, 인스타그램 등)에 로그인 되어 있을 것

### 해결 방법
1. CAPCHA 사용
2. Referrer 검증법
3. CSRF Token 사용
