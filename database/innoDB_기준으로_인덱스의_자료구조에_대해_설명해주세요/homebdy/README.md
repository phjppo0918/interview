InnoDB에서 인덱스는 B-Tree 구조로 저장됩니다.

최상위에 하나의 루트 노드가 존재하고, 가장 하위에 리프 노드, 중간에 브랜치 노드들이 존재합니다.

각 스토리지 엔진마다 리프노드에 저장되는 주솟값이 다른데, InnoDB에서는 프라이머리 키를 주소처럼 사용하므로 리프노드에 논리적인 주소를 저장합니다.
따라서 인덱스에 저장되어 있는 프라이머리 키 값을 이용해 키 인덱스를 한 번 더 검색한 후, 프라이머리 키 인덱스의 리프 페이지에 저장되어 있는 레코드를 읽어와야 합니다.