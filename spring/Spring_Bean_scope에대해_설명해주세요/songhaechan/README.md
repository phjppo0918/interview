## Bean scope

빈 스코프는 스프링 빈의 생명주기를 말한다.

기본 빈 스코프는 싱글톤으로 단 한 번 생성되고 스프링이 시작되고 끝날 때까지 계속 살아남아있다.

반면 프로토타입은 매번 새로운 빈을 생성하고 스프링 컨테이너에서 관리하지도 않는다. 종료마저 시키지않는다.

request 스코프는 웹 요청이 들어오고 나갈때까지 유효한 타입이고, session은 웹 세션이 생성되고 종료될때 까지, application은 웹 서블릿과 같은 주기로 유지된다.

주의할 점은 싱글톤과 프로토타입을 같이 사용할 때인데, 싱글톤 빈이 프로토타입빈에 의존하고 있을때 빈을 생성하면 원래 의도와 다르게 계속 같은 프로토타입빈이 조회된다.

이땐 ObjectProvider로 지정한 빈을 계속 컨테이너에서 찾아서 주입받는 방식을 사용해야한다.
