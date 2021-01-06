- ## python data type

- #### bool type

  - True(T), False(F)
  - not, and, or -> 논리연산자
  - &&, ||, ~ -> 비교연산자
  - 파이썬에서 &, |는 비트연산자를 의미함 -> 2진수로 표현
  - False로 간주하는 경우
    - "", [], (), {}, 숫자(0 이외의 숫자는 True), None

- #### set{}

  - 순서와 중복 불가능 -> 활용도 낮음

    - 중복이 되지않아 중복값 한번만 출력
    - 중복제거용으로 활용가능 -> type casting (list -> set)

  - set([]) - list 형태로 set 생성가능

  - 연산가능 - 교집합, 합집합, 차집합

    - 교집합(intersection) &, 합집합(union) |, 차집합 (difference) -

  - 요소 추가

  - ```python
    set01.add(7)
    print('set add - ', set01)
    ```

  - 요소 삭제

    - remove : 존재하지 않는 값 삭제 시 오류발생
    - discard : 오류발생하지 않음 -> 사용 지양

  - ```python
    set01.discard(9)
    set01.remove(4)
    print('set remove - ', set01)
    ```

- #### date type - 나에겐 너무 어려워

  - 패키지 설치 -> 모듈, 함수 호출

    - ```python
      from datetime import date, datetime, timedelta
      from dateutil.relativedelta import relativedelta
      from dateutil.parser import parse
      ```

    - datetime은 날짜 형식에 대한 연산불가능 -> dateutil 사용

    - year, month 관련된 옵션 필요 시 relativedelta 사용

    - parse() : 문자열 -> 날짜형식으로 변환

    - strftime() : 날짜 -> 문자열 변환 

    - ```python
      today = datetime.tdoay()
      # 날짜 -> 문자열로 변환 strftime()
      print("{}".format(today.strftime('%m-%d-%y')))
      print("{}".format(today.strftime('%m-%d-%Y')))
      ```

    - strptime() : 문자열 -> 날짜 변환

    - ```python
      strDate = '2021,01,06-11:12:40'
      userDate = datetime.strptime(strDate,'%Y,%m,%d-%H:%M:%S')
      print(type(userDate),userDate)
      ```

- #### control statement - if (조건문), for (반복문), while (반복문)

  - ##### if, if ~ else, if ~ elif ~ else, if ~ in

  - ``` python
    ''' 
    if 조건문 : 
       pass (아무것도 없을 시 pass 입력해주기)
    '''
    ```

  - list 를 이용한 if ~ in

  - ``` python
    area = ['서울', '인천', '대구', '대전', '부산']
    region = '수원'
    if region in area :
        pass
    else :
        print('{} 지역은 포함되지 않음'.format(region))
    ```

  - dict 를 이용한 if ~ in (dict는 키를 기준으로 함)

  - ```python
    areaKeyDict = {'서울' : 100, '광주' : 200}
    region = '부산'
    if region in areaKeyDict :
        pass
    else :
        print('{} 값이 존재하지 않음'.format(region))
    ```

  - 삼항연산자

  - ```python
    num = 9
    result = 0
    result = num * 2 if num > 5 else num + 2
    print('삼항 연산자 - ',result)
    ```

  - ##### loof

  - for ~ in range() / for ~ in list, dict

  - ```python
    userList = [(1,2), (3,4), (5,6)]
    for tmp01, tmp02 in userList :
        print(tmp01, tmp02, end='\t')
        userSum += tmp01 + tmp02
    print() # 개행
    print('누적 값은 : {}'.format(userSum))
    ```

    - 각각의 튜플이 2개의 값을 가지고 있음
    - list지만 안에 있는 요소가 tuple 이기 때문에 변수를 2개 지정해주어야함

  - ```python
    userDict = {'name' : 'eun', 'gender' : 'f'}
    for (key, value) in userDict.items() :
        print('{} : {}'.format(key,value))
    ```

  - List Comprehension : 여러 줄의 코드를 한 줄로 줄일 수 있음 대박적!

  - [ for 구문을 통한 반복적인 표현식 가능]

  - ```python
    userList03 = [tmp ** 2 for tmp in userList if tmp % 2 == 0]
    print(userList03)
    ```

    - for 앞쪽에 쓰는 것은 결과, 뒤쪽에 쓰는 것은 조건

  - ```python
    userDict = {'test'+str(tmp) : tmp ** 2 for tmp in range(1,10)}
    print(userDict)
    ```

    - dict에서도 적용가능

