@Controller 어노테이션에는 @Component 애노테이션이 붙어있습니다.
따라서 컨트롤러는 IoC컨테이너에 등록되어 스프링 빈으로 관리됩니다.
스프링 빈은 기본적으로 싱글톤이므로 컨트롤러 빈은 컨테이너 내에 1개만 존재하게 되며 실제 사용되는 시점에 의존성 주입을 통해 사용됩니다.
따라서 요청시마다 새로 빈을 생성하지 않고 이미 생성되어 있는 빈을 가져다 쓰므로 여러 스레드에서 컨트롤러를 사용해도 1개의 동일한 컨트롤러를 사용할 수 있습니다.