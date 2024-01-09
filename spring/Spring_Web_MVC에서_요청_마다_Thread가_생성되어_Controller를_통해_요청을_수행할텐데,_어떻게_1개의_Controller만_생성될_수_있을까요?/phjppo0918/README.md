Spring은 기본적으로 매 요청에 대해 새로운 스레드를 생성하는데, Spring은 각 요청을 병렬로 처리하기 위해 슬레드 풀을 사용합니다.

또한 Controller는 싱글톤으로 관리하고 웹 요청을 웹 스코프로 관리합니다
웹 스코프는 스프링 컨테이너가 해당 스코프 종료 시점까지 관리를 하는 것이 특징입니다.
웹 스코프는 request, session, application, websocker 등이 있습니다.