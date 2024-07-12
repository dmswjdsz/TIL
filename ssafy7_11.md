# 7_11
## 마크다운


: #으로 순서 정하기

1. 과일
    1. 딸기
    2. 포도
2. 생선
    1. 고등어
    2. 갈치

-로 카테고리 나누기
- 우산
- 의류
    - 윗도리
    - 바지
    

shift+tap : 한칸당기기

---


```python
print('hello')
print("world")
```
-> backtick 3개 : 코드넣기 ```

파이썬은 `print`함수를 사용해
텍스트를 출력한다.

 인라인 코드블럭 : backtick 두 개 ``

 mkrid

---

#### 링크 넣기

[구글](https://www.google.com)

[네이버](https://www.naver.com)

이미지는 !삽입


![pebble](https://picsum.photos/200/300)

**이미지의 너비와 높이는 마크다운으로 조절 불가 html 사용 필요**

---

**굵게**

나는

*기울임*

~~취소선~~

본문 1
---
-> 수평선 긋기
본문 2


<h1> 제목 1 </h1>

: html로 마크다운 쓰기

# 개발자로 성장하기
- 대체 어디서부터 시작해서 어디까지 해야할까?
- Python과 Java를 배우면 개발자가 되는걸까?

제일 중요한건**꾸준한 학습**을 할 수 있는 사람인지를 보여줘야한다!

#### CLI Command Line Interface
명령어를 통해 사용자와 컴퓨터가 상호 작용하는 방식
interface 소통하는 방식
#### GUI Graphic User Interface
그래픽을 통해 사용자와 컴퓨터가 상호 작용하는 방식

#### CLI
키보드만으로 모든 작업 수행 가능

. 현재 디렉토리
.. 현재의 상위 디렉토리(부모폴더)

pwd 프린트워킹디렉토리 : 현재 폴더의 위치를 확인



## Git

### Git - 분산 버전 관리 시스템
- 버전 관리 : 변화를 기록하고 추적하는 것 

    ex) google docs

- 각 버전은 이전 기록을 가지고 있음

- 중앙 집중식 : 버전은 중앙 서버에 저장되고 중앙 서버에서 파일을 가져와 다시 중앙에 업로드

- 분산식 : 버전을 여러 개의 복제된 저장소에 저장 및 관리

### 분산 구조에서의 장점
- 중앙 서버에 의존하지 않고도 동시에 다양한 작업을 수행할 수 있음

- 개발자들 간의 작업 충돌을 줄여주고 개발 생산성을 향상

- 중앙 서버의 장애나 손실에 대비하여 백업과 복구가 용이

- 인터넷에 연결되지 않아도 작업 계속 할 수 있음

- 변경 이력과 코드를 로컬 저장소에 기록하고 나중에 중앙 서버와 동기화

### Git의 영역
- 3가지 영역

    Working Directory(워킹디렉토리/작업디렉토리) : 실제 작업중인 파일들이 위치하는 영역

    Staging Area(스테이지에어리어) : W.D에서 변경된 파일 중, 다음 버전에 포함시킬 파일들을  선택적으로 추가하거나 제외할 수 있는 중간 준비 영역

    Repository(레포지토리) : 버전 이력과 파일들이 영구적으로 저장되는 영역. 모든 버전과 변경 이력이 기록됨

    버전 이름 기록 : 버전을 찍는다 
    찍는다 : commit한다고 표현
    Commit : 변경된 파일들을 저장하는 행위이며, 마치 사진찍는듯 snaptshot이라고도 표현

---

- **git init** : 로컬 저장소 설정(초기화) → git의 버전 관리를 시작할 디렉토리에서 진행
- **git add** : 변경사항이 있는 파일을 staging area에 추가 ex) git add a.txt / git add layer2_1, /add layer2_2(파일은 /추가) / git add *.txt ( 해당형식 파일이 다 올라감) / git add . (워디에 있는 모든 파일을 다 올림)
- **git rm —cashed 파일이름** : st에 있는 파일을 wd로 다시 내림
- **git commit** : staging area에 있는 파일들을 저장소에 기록. 해당시점의 버전을 생성하고 변경 이력을 남기는 것    /ex) git commit -m “Message 내용”  /  git commit -m “login기능 추가” / -m : message
- **git status** : st 현재 상태를 알려줌

---

- ls -a : 현재 폴더의 파일 목록 확인, -a는 숨김 파일 확인
- git config --global user.email "내이메일 적기"
- git config --global user.name "내이름할거 적기"
- git commit -m 'first commit’
- git status로 상태확인

내용을 수정하고 스테이징 에어리어에 올리려면; 

- git add sample.txt
- git status
- git commit -m 'second commit’
- git log: 레포짓에 쌓인 커밋 보기
- git log --oneline

; 간단하게 보여준다. 
e78350e (HEAD -> master) second commit
b08cc58 first commit

- HEAD -> master; 협업을 어디서 조인트, 머지할지를 알 수 있다.


- 로컬: 현재 사용자가 직접 접속하고 잇는 기기
- git status: 현재 로컬 저장소의 파일 상태 보기
- git log: 레포짓에 잇는 커밋 히스토리 보기
- git log —oneline
global~

#### git init 주의 사항
- 깃 로컬 저장소 내에 또다른 깃 로컬 저장소를 만들지 말것. ; 즉 이미 깃 로컬 저장소인 디렉토리 내부 하단에서 깃인잇명령어를 다시 입력하지 말것(스파게티 코드가 생김)

- 깃 저장소 안에 깃 저장소가 있을 경우 가장 바깥 쪽의 깃 저장소가 안쪽의 깃 저장소의 변경사항을 추척할 수 없기 때문.
(( 깃 인잇을 지울 방법은 없고, .git폴더를 지우자! ))

    rm -r .git/

- TIL 폴더구조를 만드는 것에는 정답이 없고, 여러 개발자의 깃헙을 방문하여 그들의 TIL을 참고해보자.

    커밋 수정하기

    git_amend

- 커밋 메세지 수정 or, 커밋 전체를 수정

git-amend-practice를 만들자
$ mkdir git-amend-practice

$ cd git-amend-practice/

$ code .

1. 커밋 메세지 수정
커밋의 해쉬 값을 확인하고(원라인으로 만들면 7자리임)

git init

touch README.md

git add

git status

git add README.md

git commit -m "기능구현완료”

git commit --amend

;; 내용 수정은 들어가서  i눌러서 insert뜨면 내용을  B 기능 구현 완료 라고 수정한다.

1. 커밋에 빠뜨린 파일을 추가
touch b-function.txt( 빠뜨린 파일)

git add .

git status

 git log --oneline

스테이징 에어리어야 있음 그래서

git commit --amend

git log --oneline : 커밋이 하나밖에 없음을 확인가능.(파일을 커밋 안에 넣었으므로)

---
### Remote Repository(원격 저장소)

코드와 버전 관리 이력을 온라인 상의 특정 위치에 저장하여 여러 개발자가 협업하고 코드를 공유할 수 있는 저장 공간

GitLab(1년동안싸피에서사용) / Github(세계1등) / Bitbucket

- 로컬&원격 저장소
    
    ‘git remote add origin ;remote_repo_url; : 로컬 저장소에 원격 저장소 추가
    
    origin : 추가하는 원격 저장소 별칭 / 별칭 사용해서 저장소 하나에 여러개 연결 가능
    

등록된 원격 저장소 목록 확인

git remote -v

fetch : 잡아채기 가져오기 

  push  밀기   pull or clone 가져오기

‘git push origin master’ : 원격 저장소에 commit 목록을 업로드

(git 아 push해줘 origin이라는 이름의 원격 저장소에 commit이라는 이름의 목록을)

원격 저장소에는 commit이 올라가는 것 commit이력이 없다면 push 할수 없다

- pulll & clone
- 

    ‘git pull origin master’ 원격 저장소의 변경사항만을 받아옴(업데이트)

    -> git pull 링크
    
    ‘git clone remote_repo_url’ : 원격 저장소 전체를 복제(다운로드)/ clone으로 받은 프로젝트는 이미 git init이 되어 있음( git  안에 다시 git init하면 안됨)
    
    -> git clone 링크

    git clone 할때 git init 중복주의

    바탕화면에서 깃배쉬 열기
    
    바탕화면에서 원격 저장소 복제 후 폴더명 git_advanced로 변경
    
    실습