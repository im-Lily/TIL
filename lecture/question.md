- ## 헷갈리는거 정리 

- dict.get() : key에 대응하는 value 값 반환

- ``` python
  # dict 생성
  dict = dict()
  dict['first'] = 123
  dict['second'] = 456
  dict['third'] = 789
  print('dictionary : ', dict)
  
  dict02 = dict.get('first')
  print('values : ', dict02)
  ```

- dict.items() : key 값으로 받음

- ```python
  userDict = {'name' : 'eun', 'gender' : 'f'}
  for (key, value) in userDict.items() :
      print('{} : {}'.format(key,value))
  ```

- ##### 헷갈림!

- ```python
  # 단어의 빈도수 구하기
  wordVec = ['love', 'word', 'cat','love', 'word', 'cat']
  print(len(wordVec)) # list의 개수 = 요소의 개수
  
  # get() : 해당 key의 value값 호출함수 - 이해안가
  wordCnt = {}
  for word in wordVec :
      wordCnt[word] = wordCnt.get(word, 0) + 1
  print(wordCnt,type(wordCnt))
  ```

- ##### nested function : 중첩함수

  - 중첩 함수가 외부 함수 영역의 자유변수에 접근 불가능

- ```python
  def outerFunc(outernum) :
      def innerFunc(num) :
          print('innerFunc - ', num)
      innerFunc(outernum + 100)
  
  outerFunc(100)
  ```

  - outerFunc에서 innerFunc을 호출함 
  - innerFunc의 매개변수 num은 실행 시 ourternum을 가져와 반환함
  - innerFunc은 outerFunc 안에서만 호출가능

- ##### closuer : 클로저

  - 중첩 함수가 외부 함수 영역의 자유변수에 접근 가능

- ```python
  def calFunc(data) :
      dataset = data
      def sumFunc() :
          total = sum(dataset)
          return total
      def avgFunc(total) :
          avg = total / len(dataset)
          return avg
      return sumFunc, avgFunc # 중첩함수 return 가능
  data = list(range(1,101))
  print('range data - ', data)
  rtnSumFunc, rtnAvgFunc = calFunc(data) # 변수가 함수로 변환가능
  tot = rtnSumFunc()
  print(tot)
  avg = rtnAvgFunc(tot)
  print(avg)
  ```

  - 중첩함수 자체를 리턴해야함 `return sumFunc, avgFunc`

    - 이해안가는 부분

    - ```python
      rtnSumFunc, rtnAvgFunc = calFunc(data) # 변수가 함수로 변환가능
      tot = rtnSumFunc()
      print(tot)
      avg = rtnAvgFunc(tot)
      print(avg)
      ```

- self-recursive function : 재귀함수

  - 함수 내부에서 자신의 함수를 반복 호출하는 기법
  - 용도 : 반복적으로 변수를 변경해서 연산할 때 (누적, 팩토리얼)

  - ```python
    def countFunc(n) : # 5 -> 1,2,3,4,5
        if n == 0 : # 종료조건
            return 0
        else :
            countFunc(n-1) # stack [5,4,3,2,1] -> 반환 시 마지막에 들어온게 가장 먼저나감
            print(n, end = ' ')
    
    countFunc(5) # 1 2 3 4 5
    ```

    - 어렵다,,!