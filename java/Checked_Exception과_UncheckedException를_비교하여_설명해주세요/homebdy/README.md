CheckedException은 RuntimeException의 하위 클라스가 아닌 예외를 의미합니다.
반드시 try/catch 또는 throw를 통해 예외처리를 해야합니다.

UncheckedException RuntimeException의 하위클래스를 의미합니다.
실행 중 발생할 수 있는 오류로, CheckedException과 달리 강제적으로 예외를 처리해야하지는 않습니다.
배열의 범위를 벗어난 경우, 값이 null인 참조 변수를 참조한 경우 발생합니다.