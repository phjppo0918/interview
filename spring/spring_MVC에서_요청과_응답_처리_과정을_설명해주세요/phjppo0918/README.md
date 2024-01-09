요청이 들어오면 Dispatcher Servlet이 요청을 받습니다.

 Dispatcher Servlet이 HandlerMapping을 통해 요청을 처리할 Controller을 탐색합니다.

 Dispatcher Servlet 이 탐색한 Controller에 맞는 Handler Adapter에게 요청을 전송합니다. Adapter은 컨트롤러가 클라이언트의 요청을 처리하도록 도와주는 역할을 합니다.

Contoller에서 요청을 처리하고, 결과를 DispatcherServlet에 반환합니다.

그 다음  Dispatcher Servlet가 ViewResolver을 통해 컨트롤러 처리 결과를 생성할 뷰를 생성하고,  Dispatcher Servlet이 View와 Model을 결합하여 응답을 제공합니다.
