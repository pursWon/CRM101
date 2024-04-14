Validation Rule
=================

Valdation Rule은 사용자가 레코드가 입력한 데이터가 저장되기 전에 지정한 rule를 충족하는지 체크하는지 확인한다.      

지정된 기준에 따라 잘못된 값이 입력될 때 Error Message도 띄울 수가 있습니다.   

예시를 하나 만들어보겠습니다.

-> Opportunity에서 User가 Administor가 아닐 때, stage를 변경 못하게 해줘.

이러면 Validation Rule의 Formula에서는

User의 field를 가져와서 설정하는 방법을 생각해볼 수 있습니다.    

Validation Rule안에서의 formula에 해당될 경우에 값 입력이나 record 저장을 막는 것이기 때문에,

formula는 이것에 부합할 경우, 진행이 되지 않습니다. 라고 보는 것이 맞다.  

```scss 

IF($User.FirstName  <>  "WONGI", ISCHANGED(StageName), false)

```

User의 firstName이 "WONGI"(Administor의 FirstName) 아닐 경우 -> true -> ISCHANGED(StangeName)

User의 firstName이 "WONGI"(Administor의 FirstName) 맞는 경우 -> false

여기서 ISCHANGED(StangeName)는 StageName을 변경할 수 없다는 제한을 걸어주는 공식입니다.

따라서 위와 같이 설정하게 되면, Administor로 로그인이 되어있지 않을 경우에는, 다음 stage로 넘어가는 것은 불가능하게끔 설정해놨습니다.
