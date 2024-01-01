웹페이지에서 실행중인 스크립트가 다른 도메인의 자원에 접근할 수 있도록 브라우저에게 허용하는 보안 기술입니다.

보안상 기본적으로 Same origin 정책을 따릅니다.

주로 HTTP 헤더에서 Access-Control-Allow-Origin, Access-Control-Allow-Methods, Access-Control-Allow-Headers 등을 통해 설정합니다.

```
Access-Control-Allow-Origin: http://trusted-domain.com
Access-Control-Allow-Methods: GET, POST, PUT, DELETE
Access-Control-Allow-Headers: Content-Type
```