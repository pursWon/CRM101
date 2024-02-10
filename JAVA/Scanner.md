# Scanner 
 
기본적인 데이터 타입들을 Scanner 의 메소드를 사용하여 입력받을 수 있다.

예로 들어 100을 입력하고자 할 때, String(문자열)로 입력받고 싶으면 next()나

 nextLine() 을, int(정수)로 입력받고 싶다면 nextInt() 를 사용하여 입력받으면 알아서 해당 타입으로 입력된다.


Scanner 을 사용할 시 util 패키지를 경로의 Scanner 클래스를 호출해야 한다.

자바에서 쓰이는 대부분의 클래스는 lang 패키지가 아니라면 import 을 통해 호출해주어야 한다.

Scanner 의 경우는 java.util 패키지에 있다.

공백(띄어쓰기) 또는 개행(줄 바꿈)을 기준으로 읽는다.

Scanner 의 입력 메소드들은 대부분 공백과 개행(' ', '\t', '\r', '\n' 등등..)을 기준으로 읽는다. 

이 덕분에 사용자의 편의에 따라 쉽게 입력을 받을 수 있다.

</br>

## Scanner Import

앞서 Scanner 의 특징에서 언급했듯이 Scanner 클래스를 사용하기 위해서는 호출해주어야 한다고 했다.

자바의 경우 java.util 패키지 안에 Scanner 클래스가 있으므로 

다음과 같이 import 를 쓴 후 해당 클래스 경로를 호출하도록 한다.

```java 

import java.util.Scanner;	// Scanner 클래스 호출

```

</br>

## Scanner 객체 생성

```java 

Scanner in = new Scanner(System.in); // Scanner 객체 생성

```

주의할 것은 Scanner 을 생성할 때 System.in 이 들어간다는 점이다.   

System.in 은 사용자로부터 입력을 받기 위한 입력 스트림이다.    

그렇기 때문에 Scanner 뿐만 아니라 다른 입력 방식들도 사용자로부터 입력을 받기 위해서는 System.in 이 들어간다.      
