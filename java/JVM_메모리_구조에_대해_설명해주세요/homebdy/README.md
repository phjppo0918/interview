JVM의 메모리 영역은 Method, Heap, Stack Area와 PC Register, Native Method Stack으로 나눌 수 있습니다.

Method, Heap Area는 모든 스레드가 공유하는 영역이며 나머지 영역은 각 스레드마다 개별적으로 생성됩니다.

첫 번째 영역인 메서드 영역은 바이트코드를 처음 메모리 공간에 올릴 때 초기화되는 대상을 저장하기 위한 메모리 공간입니다.
JVM이 동작하고 클래스가 로드될 때 적재되어 프로그램이 종료될 때까지 저장됩니다.

힙 영역은 메서드 영역과 함께 모든 스레드가 공유하는 영역으로 JVM이 관리하는 프로그램 상에서 데이터를 저장하기 위해 런타임 시 동적으로 할당하여 사용하는 영역입니다.
즉, new 연산자로 생성되는 클래스와 인스턴스 변수, 배열 타입 등의 reference type이 저장되는 곳입니다.

스택 영역은 기본 자료형을 생성할 때 저장하는 공간으로 임시적으로 사용되는 변수나 정보들이 저장되는 영역입니다.
메서드를 호출할 때마다 각각의 스택 프레임이 생성되고, 메서드 안에서 사용되는 값들을 저장하고, 호출된 메서드의 매개변수, 지역 변수, 리턴 값 및 연산 시 일어나는 값들을 임시로 저장합니다.
메서드 수행이 끝난 이후 프레임별로 삭제됩니다.

PC 레지스터는 스레드가 시작될 때 생성되며 현재 수행중인 JVM 명령어 주소를 저장하는 공간입니다.

네이티브 메서드 스택은 실제 실행할 수 있는 기계어로 작성된 프로그램을 실행시키는 영역입니다.
JIT 컴파일러에 의해 변환된 Native 코드가 해당 영역에서 실행됩니다.