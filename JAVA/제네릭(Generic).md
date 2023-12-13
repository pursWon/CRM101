제네릭(Generic)
===============

- 클래스 내부에서 사용할 데이터 타입을 외부에서 지정하는 기법   
(클래스 내부에서 사용할 데이터 타입을 나중에 인스턴스를 생성할 때 확정하여 사용함)   

- 객체의 타입을 컴파일 시에 체크하기 때문에 객체의 타입 안정성을 높이고 형변환의 번거로움이 줄어듬

제네릭의 예시

**PointList.java**

```JAVA

public class PointList {
  private Point[] pArray;
  private int crtPos;

  public PointList() {
    this.pArray = new Point[3];
    this.crtPost = 0;
 }

  public void add(Point o) {
    pArray[crtPost] = 0;
    crtPos ++;
   }
}
```
