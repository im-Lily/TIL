# Git Command

> Git 명령어 정리



# 0. init

- `git init`
- `.git/` 폴더 생성

![image-20201229151531605](./Command.assets/image-20201229151531605.png)

- `.git`폴더가 생성된 경우 오른쪽에 `master` 출력 
- 최초의 한번만 하면 됨



# 1. add

- `git add` <추가하고 싶은 파일>
  - `git add .` : 현재 폴더의 모든 파일과 폴더를 add
- working directory => staging area로 파일이동



# 2. config

- `git config -- global user.email "myemail@gmail.com"`
  - 깃헙에 올릴경우 잔디가 심어지는 기준이므로 깃헙이메일과 동일하게 적어주기
- `git config -- global user.name "myname"`
- 최초에 한번만 하면됨



# 3. commit

- `git commit -m "메세지"`
- 스냅샷 찍는 동작
- add 되어있는 파일들을 하나의 묶음으로 저장
- 메세지에 들어가는 내용은 기능 단위로 적기

# 4. remote 

- `git remote add origin <주소>`
- 원격 저장소와 현재 로컬 저장소 연결



# 5. push

- `git push origin master`
- 깃아 올려줘 origin으로 master를
- 원격저장소에 로컬 저장소의 데이터 전송



# 6. status

- `git status`
- 현재 git 상태 출력

