HashMap과 HashTable의 차이점은 동기화 보장 여부입니다.

HashMap의 경우 동기화를 보장하지 않습니다.
따라서 thread-safe하지 않아 단일 스레드 환경에서 사용하기 적합한 자료구조 입니다.

하지만 Hashtable은 동기화를 지원하여, thread-safe합니다.
때문에 멀티스레드 환경에서도 사용하기 좋은 자료구조입니다.
하지만 동기화로 인해 bloking과 unlock이 발생하여 HashMapdp에 비해 느리다는 단점이 존재합니다.

또 다른 차이점으로는 key, value에 null을 허용하는가가 있습니다.
HashMap은 key, value에 null값을 허용하지만 Hashtable은 허용하지 않습니다.