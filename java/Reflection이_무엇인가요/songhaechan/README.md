## Reflection

자바는 한꺼번에 모든 클래스를 로드하는 정적 컴파일을 사용하지않고 클래스를 사용하는 시점에 동적으로 클래스를 로드한다.
이때 클래스로더가 클래스의 정보를 JVM의 메소드 영역에 저장한다.(생성자, 변수, 메소드, 부모클래스등 여러 정보)

리플렉션은 이러한 정보를 활용하게끔 해준다.

리플렉션으로 Spring의 @Component, @Bean Lombok의 @Getter, @Setter를 사용할 수 있게된다.

리플렉션은 Java의 Class 클래스를 통해 이용할 수 있다.

1. 인스턴스가 존재 하지 않을 때 클래스.class를 통해
2. 인스턴스가 존재한다면 Class.getClass()를 통해
3. 패키지 명이 포함된 클래스 명으로 Class.forName()

Class 객체를 통해서 생성자에 접근해 객체를 생성할 수 있고, 메소드도 실행시킬 수 있다. (접근제어자에 상관이 없다.)

### ++ JVM 클래스 로드

ref - https://www.baeldung.com/java-classloaders

자바는 한꺼번에 모든 클래스를 로드하지 않고 해당 클래스가 필요한 시점에 동적으로 클래스를 로드한다.(JRE의 일부)

```java
public void printClassLoaders() throws ClassNotFoundException {

    System.out.println("Classloader of this class:"
        + PrintClassLoader.class.getClassLoader());

    System.out.println("Classloader of DriverManager:"
        + DriverManager.class.getClassLoader());

    System.out.println("Classloader of ArrayList:"
        + ArrayList.class.getClassLoader());
}
```

위 코드를 실행시키면 아래와 같은 결과를 얻는다.

```java
Classloader of this class:jdk.internal.loader.ClassLoaders$AppClassLoader@73d16e93
Classloader of DriverManager:jdk.internal.loader.ClassLoaders$PlatformClassLoader@1fb700ee
Classloader of ArrayList:null
```

Application 또는 **System ClassLoader**는 우리가 생성한 자바 클래스를 로드한다.

**extention class loader**는 DriverManager같은 코어 자바 객체의 확장된 클래스를 로드한다.

ArrayList를 보면 null로 표현돼있는데 이는 **Bootstrap Class Loader**로 모든 클래스 로더의 부모이며, Native 코드로 작성돼 있어 자바의 클래스가 아니다. 즉, 네이티브 코드로 작성된 Bootstrap 클래스로더가 자바 객체인 Class Loader를 로드한다.(중요한 놈)

Bootstrap <-- Extention <-- System

클래스로더는 위임규칙을 통해 작동한다.

클래스가 필요하게되면 System 로더로부터 Bootstrap까지 요청이 위임돼 차례로 내려오며 클래스를 찾고 System로더까지 내려와도 클래스가 존재하지않으면 ClassNotFoundException이 발생한다.
