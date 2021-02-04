- ### semi_project

- ##### DB설계

  - 요구사항 분석

  - 개념적 모델링 -> ER 다이어그램

  - 논리적 모델링 -> 정규화, SQL

  - 물리적 모델링 -> DB 내부설계, 성능에 대한 고민

  - ER 다이어그램

    ![Untitled Diagram](C:\Users\jeong\Downloads\Untitled Diagram.jpg)

- 이슈
  - 현재 내 위치 파악 -> geolocation api 이용
  - cctv -> 국도 / 고속도로 cctv 존재 
    - 이 데이터로 혼잡도, 대기시간 파악하기 어려움
    - 1차 목표 달성 후 추후에 고민
  - 1개의 회원 ID에 여러 개의 차종이 존재할 경우
    - 2차 정규화 or 차량번호
- 오전 11시 회의

- 서버 접속 후 본인 계정에서 작업

  - ssh ev@112.147.119.224

  - ev1234!

  - sudo useradd lily : 내 계정생성

  - sudo passwd lily : ek6277!

  - 접속 확인 : su - lily

  - virtualenv venv : 가상환경

  - source ./venv/bin/activate : 가상환경 들어가기

  - deactivate : 가상환경 빠져나오기

  -  mkdir data_crawling : 디렉토리 생성

  - chmod 755 dataCrawling.py : 실행권한 부여

  - vi dataCrawling.py 

  - ./dataCrawling.py

  - cp /tmp/dataCrawling.py .

  - ```python
    #!/home/lily/venv/bin/python3
    import sys
    import subprocess
    import simplejson
    
    def main():
        res = subprocess.Popen(['curl', 'https://www.keco.or.kr/kr/api/evList.ajax'],stdout=subprocess.PIPE, stderr=subprocess.PIPE)
        output , err = res.communicate()
        jsonData = simplejson.loads(output)
    
    
        forData = jsonData['list']
    
        for jsonRow in forData:
            print(jsonRow)
            exit()
    
    if __name__== '__main__':
        main()
    ```

  - ```python
    # sql connetion
    #!/home/lily/venv/bin/python3
    import sys
    import mysql.connector
    
    class DbConn:
    
        def __init__(self, profile):
            self._profile = profile
    
        def getConnectionMysql(self):
            config = {
                'user' : "ev"
                ,'password' : "Ev12341234!"
                ,'host' : 'localhost'
                ,'port' : 3306
                ,'database' : 'ev'
                ,'raise_on_warnings' : True
                ,'connection_timeout' : 60
            }
    
            cnx = None
    
            try:
                cnx = mysql.connector.connect(**config)
                return cnx
            except mysql.connector.Error as err:
                print("Connection Error")
                return cnx
    ```

  - 

- mysql workbench 접속

  - host : 112.147.119.224
  - user : ev
  - pwd : Ev12341234!
  - 