#섹션 4

### 15. Initialization
    - git init "원하는 폴더이름" : 사용자가 정한 이름의 깃 리포지토리가 생성된다
      - $ git init demo : demo 폴더가 생성된다.
    - 디폴트 브랜치 master : 깃 리포지토리가 생성됬을 때는 디폴트로 마스터 브랜치로 설정된다.
    
### 16. Local Git States

![local git state](https://user-images.githubusercontent.com/26863285/45135584-22869680-b1db-11e8-8bb5-d6a3a606f2a0.png)

    - working directory : 내가 현재 작성하고 있는 프로젝트 폴더. 어플리케이션의 모든 파일, 폴더를 가지고 있다.
    - Staging Area : Working directory에서 변경된 파일들이 Staging을 거쳐 Repository에 저장된다.
    - Repository(.git folder) : Commit 된 파일이 저장된다. Git history가 있다.
    
### 17. First Commit
    - $ touch README.md : demo 폴더에 README.md 파일 생성
    - $ vim README.md : 파일을 열어서 텍스트 입력. 저장 종료(:wq!)
    - $ git add README.md : README.md 파일을 Git Staging area에 올린다.
    - $ git commit -m "First commit" : commit을 하여 Repository(.git folder)에 저정한다.

### 18. Repository and the Git folder
     - $ ls -al : demo 폴더에서 ls -al 명령어를 치면 ".git" 폴더가 있다.
     - $ cd .git : git이 내부적으로 관리하는 폴더이다. 여기에 접속하면 (GIT_DIR!)이라고 브랜치가 나온다.
     - $ rm -rf .git : recursively, forcefully .git 폴더를 삭제한다. demo 폴더는 git init 이전 상태로 돌아가게된다
    
### 19. Start with existing project
     - $ git init . : 깃 init을 하는데 .의 의미는 현재 폴더라는 것을 뜻한다.
     
### 20. Commit and Message   
     - $ touch LICENSE.md : LICENSE.md 파일을 생성한다.
     - $ vim LICENSE.md : LICENSE.md 파일에 텍스트를 입력할 수 있다.
     - $ git add . : 여기서 .을 왜 쓰는지는 잘 모르겠음
     - $ git commit : Notepad++ 창이 뜨면서 커밋 메시지를 입력하고 저장할 수 있다.

### 21. Commit Details with Log and Show
     - $ git log : 커밋 로그를 보여주는 명령어이다.
     - $ git show : 각각의 파일들에 어떤 것들이 변경되었는지 디테일하게 보여주는 명령어
### 22. Express Commit
    - $ git ls-files : 현재 트랙킹 되고 있는 파일들만 보여준다.
                        만약 새로운 파일을 생성하고 커밋을 하지 않았다면 이 명령어로는 해당 파일이 보이지 않음.
    - $ touch new.file , $rm new.file : touch는 파일을 생성, rm은 파일을 제거
    - $ git commit -a : staging area에 add와 동시에 commit을 하는 명령어
    - $ git commit -am "update Readme" : -am을 쓰면 커밋 메시지까지 추가할 수 있다.

### 23. Backing out Changes
     - $ git reset HEAD README.md : Staging 된 파일을 Unstaging 하는 명령어. 
     - $ git checkout -- README.md : 파일이 수정되기 이전 상태로 변경하는 것. README.md 파일을 이전 상태로 바꾼다.

### 24. History and Making New Commands with Alias
     - $ git log --oneline --graph --decorate --all
        - oneline : 간략화된 커밋 내역을 볼 수 있다. 한줄로 커밋 내용 확인
        - graph : 브랜치 구조도를 볼 수 있다.
        - decorate : 어떤 커밋들이 어느 브랜치 소속인지 보여줌
        - all : 모든 브랜치의 히스토리 제공.
     - $ git config --global alias.hist "log --oneline --graph --decorate --all"
        : alias.hist는 "log --oneline --graph --decorate --all"에 별칭을 부여하는 것이다.
        그래서 위의 log~all 명령어의 별칭은 hist가 된다. 이것을 config 파일에 전역으로 등록하는 명령어이다.
     - $ git config --global --list : 내가 지정한 별칭을 config 파일의 리스트에서 찾을 수 있다.
     - $ git hist : 이제 log~all 길게 입력하지 않아도 git hist만 입력해도 로그가 나온다.
 ### 25. Rename and Delete Files
     - $ git mv example.text demo.txt : example 파일을 demo 파일로 이름을 변경한다는 명령어
        - 위 명령어를 하면 자동으로 staging으로 파일이 올라가게 된다. 변경을 적용하려면 commit을 한다.
     - $ git rm demo.txt : demo.txt 파일을 제거한다.
        - 위 명령어를 하면 자동으로 staging으로 파일이 올라간다. 변경을 적용하려면 commit을 해야한다.




