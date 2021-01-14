- ### binary 형식의 입출력

  - 객체직렬화(seriallizable) -> 파일저장
  - `import pickle`
    - mode = 'wb' -> `pickle.dump`
    - mode = 'rb' -> `pickle.load`

- ### csv, excel 파일 

  - `import pandas` -> type : dataframe

- ### xls, xlsx 파일

- ### json 파일

  - json file : 네트워크 상에서 표준으로 사용되는 파일형식
  - 구성 -> {key : value , key : value}
  - encoding : python(dict, list) -> json 문자열
  - decoding : json -> python 객체
  - `import json`
    - encoding : `json.dumps`
    - decoding : `json.loads`

- ### 코드클린 : 문자열에 대한 정규표현식을 이용하여 문자제거

  - 정규표현식 -> `import re`

  - 메타문자 : . ^ * + ? {} [] \ | ()

  - ```python
    . ^ $ * + ? {} [] \ | ()
    . -> 무엇이든 한 글자를 의미
    ^ -> 시작문자 지정
    * -> 0 or more
    + -> 1 or more
    ? -> 0 or 1
    ex)
    [abc] -> a,b,c 중 한 문자와 매치
    [^0-5] -> 0~5와 매치되지 않는 것
    ^[0-5] -> 반드시 0~5로 시작
    문자클래스
    \d -> 숫자의 자릿수
    \D -> 숫자가 아닌 문자매칭의 자릿수
    \w -> 문자+숫자
    \W -> not 문자+숫자가 아닌 문자매치
    \s -> 공백
    010-0000-0000
    ^\d{3}-\d{4}-\d{4} -> 반드시 숫자로 시작
    ```

  - `sub()`, `match()`, `search()`, `findall()`, `finditer()`, `join`
