## Restdoc vs Swagger

두 기술의 장단점을 살펴보면

restdoc은 테스트기반으로 api 문서를 자동화한다.

즉 테스트를 통과하지않은 api는 문서로 등록이 되지않아서 어플리케이션 안정성이 강화된다.

이에 비해 swagger는 테스트를 강제하지 않고, 어노테이션 기반의 api 문서 자동화 기술이다.

어노테이션을 프로덕션코드에 붙여야하기때문에 이 점이 단점으로 꼽힌다.
