#### Redshift

- ![image-20210319112455692](Redshift.assets/image-20210319112455692.png)

- ![image-20210319113228133](Redshift.assets/image-20210319113228133.png)

- OLAP, PostgreSQL 기반
  - OLTP : row 단위의 update와 insert가 잦은 서비스
  - OLAP : 규모가 큰 데이터
  - ![image-20210319151426788](Redshift.assets/image-20210319151426788.png)

- column 기반 스토리지 -> 빠른 데이터 열 검색 및 데이터 크기 감소 가능 -> 빅데이터 처리에 적합

- 정형, 비정형 데이터 수집 및 활용 가능
- 탄력적인 클러스터 크기 조정 가능 -> 비용절감
  - 워크로드 패턴에 따라 자동으로 증감
- 실시간 / 배치 레이어
  - 실시간(kinesis) / 배치(glue) 를 활용하여 데이터 수집
- 데이터 레이크 S3에 데이터 저장하여 필요한 시점에 사용가능
  - 필요한 데이터를 추출하여 Redshift에 저장하고 바인딩 뷰로 S3에 있는 데이터를 결합하여 조회가능
    - 데이터 레이크 : 데이터를 하나의 저장소로 통합하여 관리
      - 데이터 형태 및 크기와 상관없이 저장 및 분석 가능한 단일 저장소
      - 데이터 웨어 하우스(Redshift)
      - SQL 쿼리(Athena)
      - 하둡기반 빅데이터 처리(EMR)
      - 실시간 분석(ElasticSearch)
      - 시각화(Quicksight)
      - 기계학습(SageMaker)

- 타 DB와의 차이점
  - Oracle : row 기반 스토리지이기 때문에 데이터가 많아질수록 속도 느려짐, 정형 데이터만 관리하며 비용이 많음
  - Athena(서버리스) : S3에 쿼리 작업 가능 / 대용량 쿼리나 정기적 배치 처리에 부적합
  - Aurora : MySQL과 PostgreSQL 호환가능하고 속도도 빠르지만 OLTP에 적합