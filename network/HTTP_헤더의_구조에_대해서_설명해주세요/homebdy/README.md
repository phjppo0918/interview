HTTP 헤더는 크게 General Header, Request Header, Response Header, Entity Header로 나뉩니다.

먼저 General 헤더는 요청 및 응답 메시지 모두에서 사용되지만 컨텐츠에는 적용되지 않는 헤더를 의미합니다.

요청헤더는 HTTP 요청에 사용되지만 메시지의 컨텐츠와 관련이 없는 HTTP 헤더를 의미합니다.
보통 Fetch될 리소스나 클라이언트 자체에 대한 정보를 포함합니다.

Response 헤더는 서버 자체에 대한 정보와 같은 응답에 대한 부가적인 정보를 갖는 헤더입니다.

Entity Header는 컨텐츠 길이와 같은 엔티티 body에 대한 자세한 정보를 포함하는 헤더입니다.