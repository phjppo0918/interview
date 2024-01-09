filter는 servlet 스팩에서 정의 것으로 Spring과 무관하게 작동합니다., 주로 요청을 가로채서 HTTP 요청 및 응답에 대한 필터링 및 변환 작업을 수행합니다. 
cors 필터, 인코딩 필터 등을 할 수 있습니다.

interceptor은 Spring MVC에 의존하며, Spring Context에서 작동합니다.
DispatcherServlet 내에서 작동하여 컨트롤러 호출 전 후 시점에서 사용합니다.
로깅, 권한 체크, 트렌젝션 관리 등을 할 수 있습니다.