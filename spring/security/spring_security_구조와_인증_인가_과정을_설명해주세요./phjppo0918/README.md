spring security는 spring 기반 애플리케이션의 인증과 인가 같은 보안 로징을 담당하는 하위 프레임워크입니다.

spring security은 인증과 인가 대부분을 filter의 흐름에 따라 처리하고 있습니다.

처음에 사용자가 request를 보내면
AuthenticationFilter가 요청을 가로채서 가로챈 정보를 통해 UsernamePasswordAuthenticationToken(인증용 객체)를 생성합니다
그 이후 AuthenticationManager(구현체는 Provider Manager)에게 token을 전달합니다.
AuthenticationManager은 AuthenticationProvider을 조회하여 인증을 요구합니다.

AuthenticationProvider은 UserDetailService를 통해 실제 DB에서 사용자 인증 정보를 가져옵니다.

UserDetailService는 유저 정보를 찾아 UserDetails 객체를 만들어 
AuthenticationProvider에게 전달합니다.

AuthenticationProvider은 UserDetails 객체를 이용하여 인증 과정을 진행하고, 인증 완료되면 Authentication 객체를 반환합니다.

AuthenticationFilter는 Authentication 객체를 SecurityContext에 저장합니다.

스프링 시큐리티의 인가 처리는 필터 중 맨 마지막에 위치한 FilterSecurityIntercepto에 처리합니다.
AccessDecisionManager를 통해 인증, 요청, 권한 정보를 이용해 사용자에게 자원 접을을 허용여부를 최종 결정합니다.
