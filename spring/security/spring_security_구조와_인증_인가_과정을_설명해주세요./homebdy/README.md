Spring Security란 Spring 기반의 어플리케이션의 보안을 담당하는 스프링 하위 프레임워크입니다.

Security는 인증과 권한에 대한 부분을 필터 흐름에 따라 처리합니다.

1. 먼저 사용자가 로그인 정보와 함께 인증 요청을 합니다.
2. AuthenticationFilter가 요청을 가로채고, 가로챈 정보를 통해 UsernamePasswordAuthenticationToken의 인증용 객체를 생성합니다.
3. AuthenticationManger의 구현체는 ProviderManger에게 생성한 UsernamePasswordToken의 객체를 전달합니다.
4. AuthenticationManger는 등록된 AuthenticationProvider를 조회하여 인증을 요구합니다.
5. 실제 DB에서 사용자 인증 정보를 가져오는 UserDetailsService에 사용자 정보를 넘겨줍니다.
6. 넘겨받은 사용자 정보를 통해 DB에서 찾은 사용자 정보인 UserDetails객체를 생성합니다.
7. AuthenticationProvider는 UserDetail를 넘겨받아 사용자 정보를 비교합니다.
8. 인증이 완료될 경우 권한 등의 사용자 정보를 담은 Authentication 객체를 반환합니다.
9. 다시 최초의 AuthenticationFilter에 Authencation 객체가 반환됩니다.
10. Authentication 객체를 SecurityContext에 저장합니다.