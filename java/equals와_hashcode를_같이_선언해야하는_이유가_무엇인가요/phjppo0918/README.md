HashMap이나 HashSet이 해시 기반 자료구조를 사용하는데, 이들이 객체 저장 및 검색 시 객체의 hashCode를 먼저 찾은 후, equals를 사용하여 동등성을 확인합니다. 즉, 같이 선언하지 않아 equals와 hashcode가 일치하지 않으면 해시 기반 컬랙션이 제대로 동작하지 않습니다.
