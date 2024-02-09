# Relationship

오브젝트가 가질 수 있는 관계는 Lookup, Master-Detail, Many-to-Many, Self, External, Hierarchical가 존재합니다.

 관계 설정은 필수가 아니며 비즈니스와 구조와 맞게 설정하시면 됩니다. 

우선 핵심이 되는 Lookup와 Master-Detail에 대해 살펴보도록 하겠습니다.

</br></br>

## Lookup Relationship

</br>

- 1:1 관계 혹은 1:N 관계.
- 연결되어 있는 레코드가 삭제되어도 반대쪽 레코드가 삭제되지 않음
- Roll-up summary 생성 불가.
- Standard - standard / standard - custom object 연결 가능.

**<Lookup Relationship의 예시>**

- 고객정보를 담고있는 Account와 해당 고객에게서 발생하는 - 
 Opportunity: 고객 한 명이 하나의 Opportunity를 가질 수도 있고 여러 Opportunity를 가질 수 있음.

</br>

- 고객정보를 담고있는 Account와 배송정보를 담고있는 Delivery 오브젝트: 한 명의 고객으로부터 한 건의 배송 정보만 가지고 있거나 여러 배송 정보를 가질 수 있음.

</br>

- 기회 정보를 담고있는 Opportunity와 거기서 발생한 계약 정보를 담고있는 Contract 오브젝트: 하나의 Opportunity에서 한 건의 계약 정보를 가지거나 여러 건의 계약 정보를 가질 수 있음.

</br></br>

## Master-Detail Relationship

</br>

- 부모와 자식 관계 (Master and Detail).
- 1:1 관계 혹은 1:N 관계.
- 부모 레코드 삭제 시 자식 레코드도 같이 삭제됨 (strongly coupled).
- Roll-up summary 생성 가능.
- Standard object는 자식(detail)쪽으로 지정 불가.
- 오브젝트 당 최대 2개의 Master-Detail 관계 설정 가능.
- 부모 레코드에 적용되는 권한은 자식은 그대로 상속 받는다.

</br>

<Master-Detail 예시>
</br></br>
방 정보를 가지고 있는 Room 오브젝트는 이벤트 정보를 담고 있는 Event 오브젝트 레코드를 한 개 혹은 그 이상을 가질 수 있음: 방 정보가 없으면 이벤트 정보또한 존재할 필요가 없음.   

</br>

법인 고객 정보를 담고 있는 Account는 법인 담당자 연락처가 저장되는 Contact 오브젝트 레코드를 한 개 혹은 그 이상을 가질 수 있음: 법인 고객 정보가 없으면 법인 담당자 정보또한 존재할 필요가 없음.








