## Stack

Stack 과 Vector는 Collection 프레임워크가 나오기 전에 있던 자료구조다.

그만큼 최적화가 많이 이루어져있지 않다.

```java
//get
public synchronized E get(int index) {
        if (index >= elementCount)
            throw new ArrayIndexOutOfBoundsException(index);

        return elementData(index);
    }

//add
public synchronized boolean add(E e) {
        modCount++;
        add(e, elementData, elementCount);
        return true;
    }

//remove
public synchronized boolean removeElement(Object obj) {
        modCount++;
        int i = indexOf(obj);
        if (i >= 0) {
            removeElementAt(i);
            return true;
        }
        return false;
    }

// 이 외에도 거의 모든 메서드가 synchronized 처리돼있음
```

대부분의 메서드가 동기화처리가 돼 있지만, 객체자체에는 동기화처리가 돼있지않다.

그래서 사실 완벽한 동기화처리를 하지않았고 성능 저하문제도 덤이다.

심지어 get에도 동기화 돼있는걸 볼 수 있다.
