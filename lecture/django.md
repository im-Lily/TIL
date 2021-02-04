- ### Django

  - ##### MVT

    - [tistory.com](https://butter-shower.tistory.com/49)

  - New Project 생성 -> django 패키지 설치

  - terminal -> django-admin startproject baseWEB

  - `ALLOWED_HOSTS = ['localhost','127.0.0.1']`

  - `TIME_ZONE = 'Asia/Seoul'`

  - dir/w

  - cd baseWEB -> manage.py 명령어 표시(여기에서 서버실행)

  - dir/w

  - `localhost:8000` : 브라우저에서 실행

  - python manage.py startapp GreetingApp: manage.py 파일이 있는 디렉토리에서 app 생성

  - python manage.py runserver : 서버실행 명령어

    - 서버 종료 시 ctrl + c

  -  http://127.0.0.1:8000/ : 클라이언트 브라우저 이용해서 서버접속

  - 흐름 : 웹 클라이언트(Request) - URL - APP - URLS - VIEW

  - {{ment}} : print와 동일한 기능

  - http://host:port/app/view함수(urls.py)

  - url : xxx.com?key=value&key=value -> GET

  - ​                       <- querystring->

  - url : xxx.com -> POST (보안상의 이유로 post방식 지향)

  - from(action='destination' method='post|get')

  - ```python
    <body>
        <div align="center">{{ment}}</div>
        <hr/> # 바디가 없는 단독태그
        <from method="post" action="http://localhost:8000/hello/login"> # 화면 생성시 사용하는 태그
            <input type="text" name="msg">
            <input type="submit" value="send">
        </from>
        <hr/>
        <a href="http://localhost:8000/hello/baseball">야구</a><&nbsp;&nbsp;&nbsp;> #br : 개행, &nbsp; : 띄어쓰기, 절대경로
        <a href="football">축구</a><p/> # p : 단락개행, 상대경로
        <a href="">농구</a><p/>
    </body>
    ```

  - `<a href>` : 무조건 GET 방식

  - 상대경로 / 절대경로

    - 상대경로 : 현재 위치한 주소를 기준으로 붙기 때문에 ../ 로 처리해주면 됨

    - http://localhost:8000/hello/index/ 가 시작페이지이기 때문에 http://localhost:8000/hello/까지 보내야함

    - ```python
      <a href="../baseball">야구</a><br/>
      ```

    - ```python
      # view에서 url 이름지정 후 경로설정가능
      <a href="{% url 'base' %}">야구</a><br/>
      ```

  - static 위치 지정해주는 작업 : 각각의  app에 흩어져있는 static file을 한 곳으로 모으는 작업
    
    - `web> python manage.py collectstatic`
  - post 방식일 경우 꼭 해주기!
    
    -  `{% csrf_token %} `

- orm을 통한 데이터베이스 관리를 위한 계정 생성 및 접근
  - models.py 에 클래스(테이블) 생성
  - model 생성 후 admin 등록
  - `python manage.py makemigrations`
  - `python manage.py migrate`
  - `python manage.py createsuperuser`
  - -> id와 pwd 설정
  - 회원가입 페이지 생성 000에 url 작성
- views
  - HttpResponse() - x
  - JsonResponse() - json
  - render() - templates(xxxx.html)
  - redirect(path X, alias O) : 요청을 재지정함
- 사용자의 상태정보 저장을 위해서는 session, cookie 
  
  - session -> 사용자의 request가 존재한다면 계속 데이터 유지
- template 생성 시 해야하는 작업
  - `{% include 'header.html' %}`
  - `{% block content %}`
  - `{% endblock %}`
  - `{% include 'footer.html' %}`
- CRUD 작업 
  - 모델 생성 
  - admin에 생성된 모델 등록
  - `python manage.py makemigrations`
  - `python manage.py migrate`
  - `{{}}` : print
  - `{% %}` : for, if, path



