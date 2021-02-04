- #### 눈물의 cmd

- #### 서버 접속 후 본인 계정에서 작업

  - ssh ev@112.147.119.224
  - ev1234!
  - sudo useradd lily : 내 계정생성
  - sudo passwd lily : ek6277!
  - ssh lily@112.147.119.224
  - 접속 확인 : su - lily
  - root에 로그인 
    - su -
    - su - freesia : root 권한으로 freesia 계정접속
    - pwd : ev1234!
  - ll -alt /tmp : 시간순서대로 위에서부터 최신수정파일을 보여줌
  - virtualenv venv : 가상환경
  - source ./venv/bin/activate : 가상환경 들어가기
  - deactivate : 가상환경 빠져나오기
  - mkdir <폴더명> : 폴더생성
  - rm -rf <폴더/파일명> : 폴더/파일 삭제
    - rf : 옵션으로 영구삭제
  - chmod 755 <파일명> : 실행권한 부여
  - vi <파일명>
  - ./dataCrawling.py
  - cp /tmp/dataCrawling.py . : tmp(root에 있음) 폴더의 dataCrawling.py 복붙
    - dataCrawling.py . : 현재 디렉토리에 있는 파일에 접근
    - dataCrawling.py log : 하위 디렉토리에 있는 파일에 접근
  - source /home/lily/venv/bin/activate   : 본인계정 접속하자마자 가상환경으로 접속

- mysql workbench 접속

  - host : 112.147.119.224
  - user : ev
  - pwd : Ev12341234!