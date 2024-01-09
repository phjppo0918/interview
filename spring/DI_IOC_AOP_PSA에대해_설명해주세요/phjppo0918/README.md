DI - Dependency Injection - 의존성 주입
객체 간의 의존 관계를 외부에서 주입하는 디자인 패턴입니다.
즉, 자신이 사용하는 의존 객체를 직접 생성하는 것이 아니라, 외부에서 주입받아 사용합니다.
Spring에서는 Constructor, Setter, Field 등 다양한 방식으로 DI가 가능합니다

IOC - Inversion of Control - 제어의 역전
객체의 제어 권한이 개발자에서 프레임워크로 역전되는 디자인 패턴입니다.
객체의 생명 주기나 의존성 관리를 프레임워크가 담당합니다.
Spring에서는 Bean Factory 나 Applicaiton Context 등의 컨테이너를 통해 객체를 생성, 관리, 주입을 제어합니다.

AOP - Aspect Oriented Programming - 관점 지향 프로그래밍
핵심 로직에서 공통 관심사를 분리하여 모듈화 하고 적용하는 프로그래밍 패러다임입니다.
AOP에서는 프록시를 이용하여 메서드 호출 전, 후 시점에 Aspect를 적용합니다.

PSA - Portable Service Abstraction - 휴대 가능한 서비스 추상화

특정 기술에 종속되지 않도록 서비스를 추상화하여 일관된 방식으로 접근한다는 개념입니다.

JDBC Transaction등과 같은 서비스에 추상화를 제공합니다.
예를 들어 JdbcTemplate를 통해 JDBC의 추상화를 제공해 특정 DB 기술에 종속되지 않도록 합니다.

