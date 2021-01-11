- ### oop

  - 상속(is ~ a)
  - 다형성
  - 은닉화
  - 추상화

- 상속 - `super()` : 부모의 생성자 호출

  - object(최상위) < Sup(상위) < Sub(하위)

  - ```python
    class Sup(object) :
    	pass
    class Sub(Sup) :
    	pass
    ```

    - 상속 후 부모의 구성요소를 자식이 포함하여 부모에 대한 객체생성은 의미없음

- 다형성 - 상위 클래스에 정의된 함수를 하위 클래스에서 해당 함수 재정의

  - ```python
    class Person(object) :
        def __init__(self, name, age, address):
            self.name = name
            self.age = age
            self.address = address
        def perInfo(self):
            return self.name + '\t' + str(self.age) + '\t' + self.address
    
    class StudentVO(Person) :
        def __init__(self, name, age, address, stuId):
            super().__init__(name, age, address)
            self.stuId = stuId
        def stuInfo(self):
            return super().perInfo() + '\t' + self.stuId
        def perInfo(self):
            return super().perInfo() + '\t' + self.stuId
    ```

- 은닉화, 정보은닉

  - __변수 : 외부에서 변수에 대한 직접적 접근 불가능

  - ```python
    class MyDate(object) :
        def setYear(self, year):
            if year < 0 :
                self.__year = 2021
            else :
                self.__year = year
        def getYear(self):
            return self.__year
    ```
