- #### 눈물의 리눅스

- 서버 접속 후 본인 계정에서 작업

  - ssh ev@112.147.119.224
  - ev1234!
  - sudo useradd lily : 내 계정생성
  - sudo passwd lily : ek6277!
  - 접속 확인 : su - lily
  - virtualenv venv : 가상환경
  - source ./venv/bin/activate : 가상환경 들어가기
  - deactivate : 가상환경 빠져나오기
  - mkdir data_crawling : 디렉토리 생성
  - chmod 755 dataCrawling.py : 실행권한 부여
  - vi dataCrawling.py 
  - ./dataCrawling.py
  - cp /tmp/dataCrawling.py .
  - source /home/lily/venv/bin/activate   : 본인계정 접속하자마자 가상환경으로 접속

- mysql workbench 접속

  - host : 112.147.119.224
  - user : ev
  - pwd : Ev12341234!