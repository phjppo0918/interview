Hash 값을 사용하는 컬랙션인 HashMap, HashSet등의 경우 객체가 같은지 비교할 때 hashcode 값과 equals()의 리턴값을 확인합니다.

따라서 hashcode는 재정의하지 않고 equals만 재정의 할 경우, 객체의 값이 같더라도 hashcode값이 달라 서로 다른 값을 가진 객체라 판단될 수 있습니다.