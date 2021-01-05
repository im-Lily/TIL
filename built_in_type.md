- ## python data type

- #### 변수 정의 및 생성_built in type

  - int, float, bool, str 
  - 변수 타입 확인하기

- #### type casteing - 변수 타입 변경

- #### 변수 타입

  - list, dict, tuple, set, input

- #### 문자형(str) - Text Sequence 중요해!
	- list, tuple, range
  - 연속이며 인덱싱과 슬라이싱이 가능함
    - indexing 
    - slicing : 범위지정
  
- #### dir() : 사용가능한 내장함수 출력
	- replace(oldchar, newchar) : 문자치환
	- split() : 문자열 쪼개는 함수
		- return 형식은 list -> 인덱싱, 슬라이싱 가능
	- strip(), rstrip(), lstrip() : 문자열 공백 제거 함수
	- upper(),  lower() : 대,소문자 변환함수
	- endswith()
	- in, not in
	- count() : 문자의 빈도 / find() : 문자 찾기 / index() : 문자의 인덱스
	
- #### list type[]
	- sequence type이며 1차원 자료구조임
	- 순서, 중복 존재 / 수정, 삭제 가능
	- 인덱싱, 슬라이싱 가능
	- append(), instert(), extend() : 요소 추가하는 함수
		- append() VS extend()
		- append는 리스트 형태로 추가됨
		- extend는 값으로 추가됨
		- 따라서 둘의 결과 상이함
		- insert는 특정 위치에 요소 추가 가능
	- pop() : 기존 리스트에서 요소를 가져오고 삭제 조심해!
		- 마지막에 위치한 요소부터 차례대로 삭제,, 인덱스 사용하여 제거 가능
	- max(), min(), sum() : 최대, 최소, 총합
	
- #### tuple()
	- sequence type
	- 순서, 중복 존재 / 수정, 삭제 불가능
		- 수정, 삭제 불가능하기 때문에 리스트로 변경 후 수정해주어야함(casting : tuple <-> list)
	- 인덱싱, 슬라이싱 가능
	- list VS tuple
	
- #### dict{} - 헷갈리쥐
  - mapping type

  - key : value

  - 순서, 키 중복 불가능 / 수정, 삭제 가능

  - ```python
    dict01 = {
        'name' : 'eun',
        'age' : 25,
        'address' : 'incheon',
        'birth' : 970327,
        'gender' : 'f'
    }
    ```

  - ``` python
    # dict에 요소 추가하는 방법
    dict01['marriage']=False
    ```

  - ```python
    # 키 유무 판단
    print('marriage' in dict01)
    ```

  - ```python
    # dict의 value 출력
    print(dict01['address'])
    ```

  - ``` python
    # dict함수를 이용하여 여러 개의 튜플() 이용하여 리스트[] 타입으로 만들었음
    dict02 = dict([('name','eun'),('age',49),('adress','incheon')])
    ```

  - ```python
    # dict_keys, dict_values, dict_items
    # 리스트처럼 보이지만 리스트가 아님!
    # 조작하기 위해서는 casting함수 이용
    print('dict_keys - ', dict01.keys(),type(dict01.keys()),type(list(dict01.keys())))
    print('dict_values - ', dict01.values(),type(dict01.values()),type(list(dict01.values())))
    print('dict_items - ', dict01.items(),type(dict01.items()),type(list(dict01.items())))
    ```

  - ````python
    # looping
    for key in dict01.keys() :
        print('key : {} , value : {}'.format(key,dict01.get(key)))
       #print('key : {} , value : {}'.format(key,dict01[key]))
    
    for value in dict01.values():
        print('value : {}'.format(value))
    
    for (key, value) in dict01.items() :
        print('key : {} , value : {}'.format(key, value))
    ````

  - ``` python
    # 삭제 pop(), del
    del dict01['gender']
    print(type(dict01),dict01)
    print(dict01.pop('birth'),dict01)
    
    # 전체요소 삭제
    dict01.clear()
    print(dict01)
    ```

    

  

  

  

  

  

  

  

  

  

  

  

