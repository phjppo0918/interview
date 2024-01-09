java는 컴파일 되어 바이트코드(.class)로 변환합니다.

바이트 코드가 JVM 환경에서 실행됩니다.

Class loader가 class 파일을 메모리에 로드하고,
로딩된 클래스들을 runtime data area에 배치됩니다.

Execution engine이 로딩된 byte code들을 인터프리터와 jit를 통해 해석하고, 이 과정에서 byte code들을 binary code로 변경합니다. 또한, GC를 통해 메모리 영역의 메모리를 관리합니다.

# 참고
https://velog.io/@pond1029/JVM
https://pienguin.tistory.com/entry/JAVA-자바-프로그램-실행-과정-및-기본-구조
https://yoonda.tistory.com/12
