bean scope는 빈이 생성되고 유지되는 범위를 말합니다. 

기본적으로는 singleton scope를 사용합니다.

singleton scope는 애플리케이션 컨텍스트 내에서 단일 인스턴스로 유지됩니다.

prototype scope는 요청마다 새로운 인스턴스로 생성됩니다.

request scope는 각 http 요청마다 새로운 빈 인스턴스가 생성됩니다.

이 외에더 session scope, global session scope 등이 있고, 사용자가 직접 custom할 수도 있습니다.