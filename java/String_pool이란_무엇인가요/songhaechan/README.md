## String Constant Pool

String을 생성하는 방식엔 2가지가 있다.

1. new 연산자 사용
   ```java
   String str1 = new String("dog");
   ```
2. 리터럴방식 사용
   ```java
   String str2 = "dog";
   ```

두 방식엔 중요한 차이가 있다.

따옴표로 만든 str2는 JVM Heap 영역에 String pool에 들어가 상수화된다.

이후에 dog라는 문자가 리터럴방식으로 새롭게 생성되면서 String pool에 해당 문자열이 있는지 확인하고 있다면 같은 해쉬코드를 반환한다.

반면 new 연산자는 할당할때 마다 새로운 객체를 생성한다.

### 추가

원래 String pool은 Perm 영역에 존재했다.

Perm 영역은 Runtime에 메모리를 동적으로 확보하는 것이 불가능했고, OOM문제를 발생시킨다.

결국 Perm에서 Heap으로 옮기게됐고, String pool에 있는 문자열들도 GC의 대상이 됐다.
