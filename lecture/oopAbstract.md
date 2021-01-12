- ### 다중상속

  - ```python
    class Liger(Tiger, Lion) :
        def play(self):
            print('play')
    ```

  - 1차 우선순위 : 가장 먼저 정의된 부모 -> Tiger가 우선임

- ### 추상화

  - 추상 메서드를 포함한 추상클래스는 객체 생성 불가능

  - 추상 메서드는 호출할 일이 없으므로 빈 메서드로 만듦

  - 부모의 추상메서드를 상속받으면 객체 생성이 불가능하기 때문에 오버라이딩 시켜주어야함

  - 추상 클래스 상속 시 추상 메서드 모두 구현

  - `from abc import *`

  - ```python
    class Base(metaclass=ABCMeta) :
        @abstractmethod 
        def study(self):
            pass 
        def goToShchool(self):
            print('hard study')
    
    class Student(Base) :
        def study(self):
            print('공부하자')
    ```

- ### 데코레이션

  - 공통의 모듈을 외부로 빼내어 데코레이터 정의 -> 코드 간결화
  - 함수의 인자로 다른 함수를 전달
  - 데코레이터 호출방법
    - 외부함수의 인자값으로 함수를 받아서 호출
    - @decorator 입력하여 호출
  - *args, **kargs : 파라미터와 관계없이 모든 함수에 적용가능한 데코레이터 생성
  - class에서 외부의 데코레이터 사용하기 위해서는 인스턴스를 인자로 받을 수 있도록 self를 입력해주어야함

- ### 이터레이터

  - iterable object != iterator
    - iterable object : list, set, tuple, dict, text sequence (collection)
    - iterator : 순차적으로 다음 데이터 리턴이 가능한 객체 
      - iter(), next() -> 순환하는 다음 값 반환

- ### 제너레이터

  - iterator를 만들어주는 기능 -> yield 

  - 메모리 성능 위하여 루프를 컨트롤하기 위해 쓰이는 루틴

  - ##### Generator Comprehension () -> (Lazy Operation)

    - (출력형식 for 요소 in collection)

- ### Comprehension

  - [출력표현식 for 요소 in sequence [if 조건식]] -> list type
  - {출력표현식 for 요소 in sequence [if 조건식]} -> set type
  - {key-value for 요소 in sequence [if 조건식]} -> dict type