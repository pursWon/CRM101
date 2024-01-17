SQL의 기본 개념
============================

**데이터 정의어 (Data Definition Language)**

: DB의 구조를 정의함    

</br>

**CREATE** : 테이블 생성

**ALTER** : 테이블 수정

**DROP** : 테이블 삭제 (테이블 구조까지 아예 삭제됨, 롤백 불가)    

**TRUNCATE** : 테이블의 모든 행 삭제 (테이블 구조는 그대로, 데이터만 삭제)   

</br>

**데이터 조작어 (Data Manipulation Language)**

: DB의 레코드를 조작해서 조회, 삽입, 수정, 삭제가 이루어짐    

SELECT : 데이터 조회   

</br>

```SQL

SELECT 속성명
FROM 릴레이션
[WHERE 조건]
[GROUP BY 속성명]
[HAVING 그룹조건]
[ORDER BY 속성 [ASC | DESC] ];

```

</br>

INSERT : 데이터 삽입

```SQL

INSERT INTO 릴레이션(속성명)
VALUES(데이터)

```

</br>

DELETE : 데이터 삭제 (롤백 가능)

```SQL

DELETE FROM 릴레이션
[WHERE 조건]; --WHERE이 생략되면 해당 릴레이션 내 모든 튜플 삭제

```

</br>

UPDATE : 데이터 수정

```SQL

UPDATE 릴레이션
SET 속성명 = 데이터
[WHERE 조건]; --WHERE절 생략되면 해당 릴레이션 내 모든 튜플 수정

```

</br>

**데이터 제어어 (DCL, Data Control Language)**

: DB의 접근권한 및 트랜잭션을 제어함   

```SQL

GRANT 권한 ON 테이블 TO 사용자
[WITH GRANT OPTION]; --다른 사람과 권한을 나눠가질 수 있는 옵션

```

</br>

REVOKE : 권한을 회수

```SQL

REVOKE 권한 ON 테이블 FROM 사용자
[CASCADE CONTRAINTS]; --연쇄적인 권한 해제(WITH GRANT OPTION으로 부여된 것까지 취소)

```



