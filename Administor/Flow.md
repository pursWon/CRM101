Flow
=============================

no code로 어렵지 않게 click으로       

Flow를 만들고 사용함에 따라 자동화가 이루어지는 것이 Flow가 가지는 강점입니다.     

예를 들면, Sales 부서에서 트러블 슈팅이나 고객 이슈에 관해서 바로 알 수 있게끔 Flow를 만들어 놓는다면 바로 해당 문제를 받고 문제 해결에 돌입할 수 있습니다.    

Flow의 종류에는 총 6가지가 있습니다.        

가장 많이 사용하는 유형의 Flow는 Screen Flow와 Record Trigger Flow가 있습니다.    

</br>

1. Screen Flow
    - Flow를 만들어서 Screen에 보여줄 수 있습니다. 큰 톱니바퀴에서 edit page를 눌러 Lighting App Builder 화면으로 넘어간 후에 Flow를 Screen에 보여주게끔 설정 가능
    - 예시 : Account Page에서 Opportunity Wizard를 만들어서 미팅이 끝난 후 바로 Opportunity를 설정할 수 있게끔 만들어 놓는다.
2. Record Trigger Flow
    - field를 Create, Update, delete할 때 업데이트 할 수 있게끔 만드는 Flow
    - 설정 방법
        - back에 들어가서 quick box에 flow로 검색해서 flows에 들어감
        - 언제 업데이트를 해줄 것인지→ create, update, create or update, delete
        - condition → OR, AND, Formula evaluates true, Custom Logic
        - Optimize Flow : Fast Field Upedate → 빠르게 field만 업데이트 할 때 사용, field만 업데이트 하면 되므로 before Save가 이루어짐, Actions related Records는 action, record 모두 업데이트 사용하므로 after save가 이루어짐
3. Sceduled Trigger Flow
    - 예시 : 내일 오후 3시쯤에 자동으로 이메일을 발송하고 싶을 때 해당 Flow를 사용
4. Platform event triggered flow
    - 예시 : 외부 회사나 업체를 주로 platform으로 가리킴. 예를 들면,  물건 배송이 누락되었으면 해당 flow를 발동함
    
5. Autolaunched Flow
    - 예시 : trigger 없이 flow를 발동
6. Record Triggered Orchestration
    - 예시 : record가 병행되서 trigger 일어날 수 있음

</br>

Resource : Variable, Constant, Formula 등 Flow 전체가 참조할 수 있는 것    

Flow를 다 만든 후에는 debug & Test가 이뤄줘야합니다.     
