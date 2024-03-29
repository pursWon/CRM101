생성자(Constructor)
======================

- new 연산자와 같이 사용되어 클래스로부터 객체를 생성할 때 호출되고 객체의 초기화를 담당 한다.
- 생성자를 실행 시키지 않고 클래스로부터 객체를 만들 수 없다.
- 생성자가 성공적으로 실행되면 JVM의 Heap영역에 객체가 생성되고 객체의 참조 값이 참조변수에 저장 된다.
- 몇 가지 조건을 제외하면 메소드와 같다.
- 모든 클래스에는 반드시 하나 이상의 생성자가 있어야 한다.

**생성자의 정의**   

- 생성자의 이름은 클래스와 같아야 한다.
- 생성자의 리턴값이 없다. (하지만 void를 사용하지 않는다.)

</br>

```java

public class Goods { public Goods() {
  // 초기화 코드
}

public Goods( String name, int price ) {
  // 초기화 코드 }
}

```

</br>

- 매개변수가 없는 생성자
- 클래스에 생성자가 한 개도 정의되어 있지 않으면 컴파일러가 기본생성자를 추가한다.
- 생성자가 한 개라도 있으면 기본생성자를 추가 하지 않는다.
- 여러 개의 생성자를 사용할 수 있다. -> **생성자 오버로딩**
