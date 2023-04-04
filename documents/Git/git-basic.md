# Git

- git init : Initialize repository
- .git : git repository
- git status : git working tree status
- git add : add to staging area
- git commit  : create version
- git log : show version
  - git log --stat
  - git log --all
  - git log --graph
  - git log --oneline
- git diff : Show changes
- git log -p
- git checkout / git switch 
- git commit -am "34" : add과 commit을 동시에 
    * 한번이라도 commit이 된 파일만 사용 가능 
- git reset : 삭제하기 
    * --hard : 가장 강력한 삭제 
- git revert : 되돌리기

## git branch
- git branch "이름" : branch 생성
- git branch -d "이름" : branch 삭제
- git merge AA
    * 현재 있는 브랜치에 AA 브랜치 내용을 merge
- git merge --abort 
    * merge를 중단할 수 있음 (conflict 상황에서 사용 가능)
    * 생각보다 자주 사용 
- git checkout -b 브랜치명
    * 브랜치 만들고, 전환까지 동시에 하기 

***
- 공유되기 이전 버전들만 git reset 할 수 있음 
    * 그렇지 않을 경우 엉키는 여러 문제점 들이 발생할 수 있음 

***
- tool
- .gitignore
- branch
- tag 
- backup

***
## 필기노트   
  

git pull == git fetch origin main + git merge origin/main   
모달창

## branch
### 정의
- 영어사전: 가지
- git에서의 정의: A branch in Git is simply a lightweight movable pointer to one of these commits.
- 실무에서: 새로운 작업(기능 개발, 버그 수정 등)을 시작할 때 만든다.

### 명령어
1. 브랜치 생성 : `git branch 브랜치 이름`
2. 생성되어 있는 브랜치 보기
    * `생성 되어있는 브랜치 보기`
3. 다른 브랜치로 전환하기
    * `git checkout 브랜치명`
    * `git switch 브랜치명`
4. 브랜치 만들고, 전환까지 동시에 하기
    * `git checkout -b 브랜치명`

## 작업 프로세스
> 공동 작업을 할 때는 다음과 같은 프로세스로 진행한다.
1. 이슈를 만든다.
2. 이슈에 해당하는 브랜치를 만든다.
3. 2에서 만든 브랜치에 커밋을 만든다.
    * 이때 커밋 헤시지엔 이슈 번호를 적어서, 이슈 트래커와 커밋을 연동시킨다.
4. git push 명령어를 사용해서 작업 중인 브랜치에 있는 모든 커밋들을 원격 저장소에 push 한다.
    * `git push -u origin 브랜치이름`
    * `git push`
5. 원격 저장소에서 Pull Request(Merge Request)를 생성한다.
6. 코드 리뷰를 받는다(선택).
7. PR(Pull Request)를 마무리 한다(Merge).

## 로컬 저장소와 원격 저장소 동기화하기

### fetch
- git fetch 명령어를 사용하면 로컬 저장소의 브랜치에 있는 커밋들을 원격 저장소에 특정 브랜치로 push해서 동기화 할 수 있다.

### push
- git push 명령어를 사용하면 로컬 저장소의 브랜치에 있는 커밋들을 원격 저장소에 특정 브랜치로 push해서 동기화 할 수 있다.

임시 저장할 때 쓰는 명령어   
git stash