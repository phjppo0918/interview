## AOP vs Interceptor

AOP와 Interceptor 모두 공통적인 처리를 한 곳에 묶어서 관리한다는 점에서는 비슷하다.

Interceptor는 DispatcherServlet이 컨트롤러의 handler를 호출하기 전/후에 요청을 가로채 인증,권한체크와 같은 공통적으로 적용해야하는 로직을 한 곳에서 관리할 수 있다.

반면 AOP는 비즈니스로직 메서드가 실행되기 전/후에 실행된다. 프록시패턴으로 실행되며 interceptor와 aop는 적용되는 위치가 다르다.
