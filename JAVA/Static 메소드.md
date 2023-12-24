Static 메소드
===============

- 전역변수와 전역함수를 만들 때 사용
- 모든 클래스에서 공유하는 전역 변수나 전역 함수를 만들어 사용할 수 있다.
- 객체를 생성하지 않고 접근할 수 있다.
- static 메소드에서는 this 사용 불가
- static 메소드에서는 static 멤버만 접근할 수 있다.

</br>

```Java

public class MyMath {
    public static double PI = 3.14;
    public static int plus(int a, int b) {
      return a+b;
    } 

    public static double plus(double a, double b) {
      return a+b;
    }

    public static double CircleArea(int radius){
      return radius*radius*PI;
    } 
}

MyMath.PI = 3.14
MyMath m = new MyMath();
m.PI
```
