- ### DDL(CREATE, DROP, ALTER) 

- ### DML(INSERT, UPDATE, DELETE)

  - 테이블 생성(제약조건)
    - INSERT INTO TABLE_NAME([컬럼리스트]) VALUES(VALUE, VALUE) ;
  - 제약조건(NOT NULL - 컬럼 레벨 제약만 가능, UNIQUE, PRIMARY KEY, FOREIGEN KEY, CHECK)
    - 제약조건 설정방법 : 테이블 레벨, 컬럼 레벨

  ```sql
  CREATE TABLE TABLE_NAME(
  	COLUMN_NAME DATETYPE [DEFAULT EXPRT][CONSTRAINT],
  	TABLE_CONSTRAINT)
  ```
  - 기본키를 네이블 내 하나만 존재

  - 테이블 레벨에서 조합하여 여러 개의 기본 키 가능

  - 기본키 : 데이터의 무결성 

    - 중복 허용X, NULL 값 허용X

  - 외래키 : 부모에 의존하는 데이터이거나 NULL 값 허용

    - `REFERENCES 부모테이블(컬럼명)` 

  - DROP TABLE 테이블명

  - ```sql
    UPDATE TABLE_NAME
    SET [COLUMN_NAME = VALUE,]
    WHERE CONDITION ;
    ```