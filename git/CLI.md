# Git 공부 (21.12.02)

## 설치하기

Git-Bash 프로그램 설치



## Git-Bash 프로그램 실행

### 처음 실행화면

![image-20211202144826361](CLI.assets/image-20211202144826361.png)

파일 생성 등 작업은 홈 폴더(기본 저장소)에 저장

### 기본 저장소

C:\Users\owner

*사용자 컴퓨터마다 다를 수 있음*

![image-20211202144406742](CLI.assets/image-20211202144406742.png)



## 명령어

### 파일 생성

- `touch` 명령어를 사용하여 **filename** 이름의 텍스트 파일 생성

- ```shell
  touch filename.txt
  ```

- 명령어 입력 화면

  - ![image-20211202144901313](CLI.assets/image-20211202144901313.png)

- 파일 생성 확인 화면
  - ![image-20211202145127787](CLI.assets/image-20211202145127787.png)





### 폴더 생성

- `mkdir` 명령어를 사용하여 **CLI** 이름의 폴더 생성

- ```shell
  mkdir CLI
  ```

- 명령어 입력 화면
  - ![image-20211202145510051](CLI.assets/image-20211202145510051.png)

- 파일 생성 확인 화면
  - ![image-20211202145628369](CLI.assets/image-20211202145628369.png)



### 파일 이동

- `mv`명령어를 이용하여 filename.txt 파일은 CLI 폴더로 이동

- ```shell
  mv filename.txt CLI/
  ```

- 명령어 입력화면

  - ![image-20211202145820684](image-20211202145820684.png)

- 파일 이동 확인 화면

  - ![image-20211202145933856](CLI.assets/image-20211202145933856.png)



### 작업창 이동

- `cd` 명령어를 이용하여 작업창을 이동
  현재 작업창 홈 폴더(~)에서 CLI 폴더 안으로 이동
  *window에서는 폴더를 더블클릭해서 들어가는 개념으로 생각*

- ```shell
  $ cd CLI
  ```

- 명령어 입력 화면

  - ![image-20211202150235486](CLI.assets/image-20211202150235486.png)

- 폴더 한단계 위로 올라가기
  윈도우에서는 **↑** 기호로 보면 됨

  - ```shell
    $ cd ..
    ```

- 바로 홈폴더(~)로 가기

  - ```shell
    $ cd
    ```

- 



### 폴더 내 파일 보기

- `ls` 명령어를 이용하여 현재 작업창(폴더)내에 있는 파일 보기

- ```shell
  $ ls
  ```

- 명령어 입력 화면

  - ![image-20211202150814132](CLI.assets/image-20211202150814132.png)

  - CLI 폴더 내 filename.txt 파일이 있는걸 확인할 수 있음.



### 파일 삭제

- `rm` 명령어를 이용하여 파일 삭제 (단, 휴지통으로 이동이 아닌 완전 삭제)

- ```shell
  $ rm filename.txt
  ```

- 명령어 입력 화면

  - ![image-20211202173402892](CLI.assets/image-20211202173402892.png)

- 파일 전체 삭제

  - *을 사용하여 해당 폴더 안에 있는 모든 파일 삭제

- ```shell
  $ rm *.txt
  ```

### 숨긴파일 만들기

- 윈도우에서는 보이지만, 유닉스에서 숨긴파일 만들기

- ```
  $ touch .hidden.txt
  ```

  - 파일명에 .을 붙여서 만들면 `ls`했을때 안보임
    단, 윈도우에서는 보임

- 안보이는 파일을 보려면

- ```shell
  $ ls -a
  ```

- 안보이는 파일 지울때

- ```shell
  $ rm .hidden.txt
  ```

- 



\#안보이는 파일 지울때

\#rm .hidden.txt / 그냥 파일 삭제와 같음



\#tab을 누르면 자동완성

\#대소문자 구분 안함



\#폴더 or 디렉토리 삭제

\#rm은 파일 삭제 / 폴더 or 디렉토리 삭제 안됨

\#rm -r cli / 폴더 or 디렉토리 삭제

\#rm -r cli



\#code . / .은 지금 내가 있는 폴더 / 지금 내가 열고 있는 폴더를 code로 열어줘 / vscode 여는게 code

code .



# 수업 내용 막 적어

GItHub은 파일 관리가 아닌 폴더(디렉토리) 관리 Tool로 보면 됨

Git-Practice 이 폴더(디렉토리)를 Git에서 관리한다고 보면 됨

기존 폴더(디렉토리)는 파일을 가지고 있는 그 이상도 이하도 아님

폴더(디렉토리) -> 저장소(레포지토리) 업그레이드해서 기능을 추가하겠음

```shell
$ git init
```



를 통해서 (master) 글자가 나오면서 디렉토리가 레포지토리가 됨.

상위폴더는 레포지토리가 아닌 디렉토리 그대로임.

하위폴더는 레포지토리로 만들어짐

홈폴더를 레포지토리(git init)을 하면 절대 안됨.

내가 관리하는 폴더 확인 할것!



Ctrl L 누르면 터미널 창 위로 올려서 깨끗하게 보기

git init을 하면 .git 폴더가 생김

숨긴 폴더라서 ls -a로 확인 가능

.git폴더가 생기는게 레포지토리로 업그레이드 된것이므로 rm -rf .git로 .git폴더를 삭제해서 다운그레이드 가능 (초기화) (홈폴더를 레포지토리 하게 되면, 그때 사용)

*가능하면하지 말것*



리포안에서 리포하지 말기

git-practice를 리포했는데 거기서 mkdir로 폴더 만들었는데

그 폴더 다시 git init하지 말기



$ git init 입력 전 확인할 점

1. ~인지 확인하기
2. (master) 떠 있는지



git status 

git의 현재 상황을 말해줘

No commits yet

지금 아무것도 없어요

README.md 파일 생성 후 gti status

빨간글씨: commit에 안올라가있어

Untracked files:

추적하지 않는다

commit하려면 git add해라

git add README.md

했더니 빨간글씨가 초록색 글씨로 바뀜

git config --global user.email 'kim92sb@gmail.com'

git config --global user.name 'leo kim'

cat ~/.gitconfig

내 이름과 이메일 잘들어가있는지 확인



code ~/.gitconfig

가서 이름과 이메일 수정해줘도 됨.

'를 누르고 치다가 '를 안닫으면

계속 > 가 나오면서 무한 엔터 표시... 이럴땐 Ctrl C ( ^C 로 보임)를 눌러서 취소하면 됨.



초기화 시점에 1회 입력

```shell
$ git init
```

작업하며 계속 입력

```shell
$ git add <filename>
$ git commit -m 'MESSAGE'
```

모니터링 명령어

```
$ git status	# 현재 상황
$ git log		# commit log
```



git은 변경사항에 매우 민감하다

untracked files:

처음보는 파일이라서 몰라요

한번이라도 얼굴도장(스테이징 한 파일/add해라)한 파일만 가능함



git restore --staged README.md

READMD.md 파일을 스테이지에서 다시 내려줘

이전 commit과 지금 commit을 비교해줌 (빨간색과 초록색)



```
$ git add . # 내 위치(.)에 있는 모든 파일을 add해라
```



바로 commit하지 않고 스테이징하고 commit하는 이유는 묶어서 commit하기 위해서!



파일 3개를 묶어서 commit하기 (파일 3개는 신입사원 안내 문서 생성)



git log 했을때 내용이 너무 길어서  : 나오면 q를 누르면 된다

commit할때 메세지 없으면 이상한 창이 나옴

그때는 esc 계속 누르다가 :q!로 나오기



git init

git add .

git commit -m 'first commit'

$ git remote add origin "git주소"

=> 컴퓨터에 있는 로컬저장소와 github에 있는 원격저장소를 연결시킴

$ git push -u origin master



# 21.12.03

## 원격 저장소(remote repo) 등록하기

```shell
$ git remote add origin <URL>
```

 하나의 origin을 여러 URL에 remote 할 수 있다.

- 하진 하나를 여러 드라이브에 저장 할 수 있다.
- 원격 저장소 이름이 origin

## 원격 저장소에 PUSH하기

```
$ git push origin master
```

 
