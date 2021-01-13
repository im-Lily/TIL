- ### composition(Aggregation)

  - 상속을 회피하고 클래스의 일부 기능을 그대로 활용하고 싶을 때 사용
  - 상속관계가 복잡할 경우 코드 이해 어려움
  - 컴포지션은 명시적 선언, 상속은 묵시적 선언

- ### Exception(예외처리)

  - ```python
    try :
    	에러가 발생할 가능성이 있는 코드
    	정상코드
    	에러가 발생할 가능성이 있는 코드
    	정상코드
    except Exception or xxxError :
    	1. 프로그램의 흐름을 정상으로 컨트롤 -> 운영단계
    	2. 예외발생에 대한 디버깅 -> 개발단계
    	3. 로그파일 생성하여 예외정보 저장 -> 개발단계
    except Exception or xxxError :
    	각각의 에러를 잡기위한 객체정의(에러발생개수와 동일하게)
    else :
    	에러가 발생되지 않을 때 실행되는 블럭
    finally :
    	에러발생과 상관없이 항상 실행
    ```

  - 리스트, 함수, 클래스에서 예외처리 가능

  - 강제 예외 발생 -> `raise Exception`

  - 사용자 정의 예외 클래스 -> `Exception` 상속

    - ```python
      class InsufficientError(Exception) :
          def __init__(self, msg):
              self.msg = msg
      ```

- ### Collections.namedtuple('실제 클래스 이름', (변수) [변수])

  - 클래스없이 객체 생성방법(변수만을 생성)

  - 클래스와 다름 -> 클래스는 인스턴스 소유의 변수와 함수를 생성

  - `import collections`

  - ```python
    Person = collections.namedtuple('Person', 'name, id') # string
    per = Person('eun', 100)
    print(per,type(per))
    ```

  - 속성에 접근하는 방법

    - 인덱스로 접근

    - ```python
      print('idx 0 -', per[0])
      ```

    - 직접 접근

    - ```python
      print(per.name)
      ```

    - ```python
      name, id = per
      print(name, id)
      ```

- ### 파일 입출력

  - `open(file = '파일경로/파일명', 'mode = 'r|w|a')`
  - `file.close()` 항상 해주어야함
  - `with open () as file` -> 자동으로 close 해줌

