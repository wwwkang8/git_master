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
    
