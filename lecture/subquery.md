- ### SET OPERATOR

  - 두 개 이상의 쿼리 결과 하나로 결합
  - SELECT절에 기술하는 컬럼 개수와 데이터 타입은 동일해야함
    - DUMMY CLOUMN 사용
  - UNION / UNION ALL / INTERSECT / MINUS

- ### 서브쿼리()

  - SELECT, FROM, WHERE, HAVING 절에서 사용
  
  - 단일 행 : 단일 행 반환
    
    - 단일 행 연산자 : >, >=, <, <=, <>
    
  - 다중 행 : 여러 행 반환
    - 다중 행 연산자 : IN, NOT IN,  ANY, ALL
    - 다중 행 서브쿼리에서 NULL 값 존재 시  NULL 값 제거
    
  - 다중 행 서브쿼리 ANY, ALL 연산자
    - `< ANY : 비교 대상 중 최대값 보다 작음`
    - `> ANY : 비교 대상 중 최대값 보다 작음`
    - `< ALL : 비교 대상 중 최소값 보다 작음`
    - `> ALL : 비교 대상 중 최대값 보다 큼`
    
  - #### 상관관계 서브쿼리 
  
    - 메인 값 받아 서브 실행 -> 다시 메인 실행

	- #### EXISTS, NOT EXISTS 연산자
	  - 결과에 포함되는지 여부 확인
  
    
  
    