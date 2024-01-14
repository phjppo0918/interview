서블릿이란 동적 웹페이지를 만들 때 사용되는 자뱌 기반의 웹 애플리케이션 프로그래밍 기술입니다.

클라이언트가 요청을 하면 그에 대한 결과를 다시 전송해주는 역할을 합니다.

1. 먼저 사용자가 url을 입력하면 HTTP Request가 서블릿 컨테이너로 전송됩니다.
2. 요청을 전송받은 서블릿 컨테이너는 HttpServeletRequest, HttpServletResponse 객체를 생성합니다.
3. 이후, web.xml을 기반으로 사용자가 요청한 URL이 어느 서블릿에 대한 요청인지 찾습니다.
4. 해당 서블릿에서 service메서드를 호출한 후 클라이언트의 GET, POST 여부에 따라 doGet, doPost()를 호출합니다.
5. doGet, doPost 메서드는 동적 페이지를 생성한 후 HttpServletResponse객체에 응답을 보냅니다.
6. 응답이 끝난 이후 HttpServletRequest, HttpServletResponse 두 객체를 소멸시킵니다.