Method Area, Heap, Stack, PC Register, Native Method Stack으로 이루어져있습니다.
이 중 Stack, PC Register, Native Method는 스레드 단위로 관리합니다.

method Area는 jvm이 실행되면서 생기는 공간으로, Class 정보, 전역 변수, static 변수 등이 저장됩니다.

Heap은 new 연산자로 생성된 객체, Array 같은 동적 생성 데이터 같이 Reference Type 데이터들이 저장되는 공간입니다.

Stack은 지역 변수, 메셔드의 메개변수 같이 잠시 사용되고 메서드 종료시 사라지는 데이터들이 저장되는 공간입니다.
만약 지역변수이지만 reference type인 경우는 heap에 저장된 데이터의 주소값을 저장합니다.

PC 레지스터는 스레드가 생성되면서 생기는 공간으로, 스레드가 어느 명령어를 처리하고 있는지 죽, JVM이 실행하고 있는 현재 위치 주소를 저장하는 레지스터입니다.

마지막으로 Native Method Stack은 java가 아닌 다른 언어로 구성된 메서드를 실행이 필요할 때 사용되는 공간입니다.