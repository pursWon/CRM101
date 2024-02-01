Access and Object Security
==============================

## Object

빌딩 → Org

회사에 들어가는 것 → Object

회사 안에 내 자리를 찾아가는 것 → Record

내 자리를 찾아가서 책을 피는 게 → Field

Object Permission은 사용자들이 빌딩의 어느 층에 출입할 수 있는지 지정해주는 것

</br>

## Profile


Profile을 통하여 User에게 객체와 데이터를 어떻게 접근할 수 있는 지에 대한 정의를 할 수 있다.

하나의 Profile은 한 명의 User에게 할당이 가능하다.

User가 로그인을 함에 있어서 Org 내에 신뢰할 만한 IP-Ranges 가졌다면 로그인 성공.

아닐 경우에, Authentication 유무를 물어보는데 없다면 로그인에 실패.


</br>

## Permission Sets

Permission Sets를 사용하기 위해서는 BACK에 들어가서 Search box에서 User를 검색한 후에, 

Manage Assignment 버튼을 눌러서 할당을 할 수 있다.  

Object 접근에 대한 권한을 Applicants, Interviewers, Jop Applications 등에게 부여할 수 있다.

Job function에 따라 여러개의 permission set를 하나의 그룹으로 만들 수 있다.

Muting Permission은 permission set group에 추가한다면 해당 그룹에 속한 User들은 Muting으로 지정한 권한에 접근을 할 수 없게 된다.

(인턴인 Brandon 씨가 어떠한 records도 삭제하지 못하게끔 하려면 → Brandon씨가 속한 Permission set Group에 Delete 기능을 지정한 Muting Permission을 집어넣으면 된다!)

Q. Admin이 개인 사용자에게 permission set를 할당하는 이유는 무엇인가요?

- 그들의 profile이 허용하는 범위보다 더 많은 권한을 부여해주기 위해서입니다.


</br>

## **Field-Level Security**

사용자들이 그들의 Profile에서 어떤 field를 볼 수 있고 편집할 수 있는 지, 또 permission sets를 할당할 수 있는지 control 하게끔 하는 기능.
