## == vs equals
자바에서 == 는 객체의 해시값을 통해 동일성을 검사하고, equals는 객체의 값을 통해 객체의 동일성을 검사한다.
하나의 예시로 Wrapper 클래스 같은 값의 Integer 끼리는 == 비교를 하게되면 결과값이 False이다.
같은 상황에서 equals 비교를 한다면 결과값이 True이다.


### ++ Integer Caching
 사실 Integer, Long 같은 클래스는 내부적으로 캐싱하기때문에 작은 수를 비교한다면 위 이야기가 맞지 않을 수 있다.