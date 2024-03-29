1. 먼저, 클라이언트가 서버에 요청을 하면, 프론트 컨트롤러인 디스패처 서블릿 클래스가 요청을 받습니다.
2. 디스패처 서블릿은 프로젝트 파일 내의 servlet-context.xml 파일의 @Controller 인자를 통해 등록한 요청 위임 컨트롤러를 찾아 매핑된 컨트롤러가 존재하면 @RequestMapping을 통해 요청을 처리할 메서드로 이동합니다.
3. 컨트롤러는 해당 요청을 처리한 서비스를 받아 비즈니스 로직을 서비스에게 위입합니다.
4. 서비스에서는 요청에 필요한 작업을 수행하고, 요청에 대해 DB에 접근해야 한다면 DAO에 요청하여 처리를 위임합니다.
5. DAO는 DB 정보를 DTO를 통해 받아 서비스에게 전달합니다.
6. 서비스는 전달받은 데이터를 컨트롤러에게 전달합니다.
7. 컨트롤러는 모델 객체에게 요청에 맞는 뷰 정보를 담아 디스패처 서블릿에게 전송합니다.
8. 디스패처 서블릿은 ViewResolver에게 전달받은 뷰 정보를 전달합니다.
9. ViewResolver는 응답할 뷰에 대한 JSP를 찾아 디스패처 서블릿에게 전달합니다.
10. 디스패처 서블릿은 응답할 뷰의 Render를 지시하고 뷰는 로직을 처리합니다.
11. 디스패처 서블릿은 클라이언트에게 랜딩된 뷰를 응답하며 요청을 마칩니다.