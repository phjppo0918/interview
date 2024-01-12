## 예외 처리

Interceptor는 Spring Context 안에 있기때문에 Controller Advice에 Exception Handler를 등록하면 전역 예외 처리가 가능하다.

위 방식이 가장 많이 사용하는 방식이다.

하지만 Filter단은 spring context 밖에 있기 때문에 Controller advice로 예외를 처리할 수 없다.

Filter에서 예외가 발생하고 잡지않으면 WAS까지 예외가 올라가기 때문에 예외가 발생한 필터 앞에 예외처리해주는 필터를 필터체인에 추가해서 해결해야한다.
