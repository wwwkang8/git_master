### 68. Creating Branches on Github
    - Github 페이지에서 좌측 상단에 드롭다운 버튼을 누르면 현재 브랜치를 볼 수 있다.
    - 브랜치를 검색해서 있다면 해당 브랜치를 보여주고 없다면 새로운 브랜치를 생성한다.
    - master 브랜치와 다른 브랜치는 독립적으로 존재한다.

### 69. Local Branches
    - $ git checkout -b remove-ipsum : remove-ipsum이라는 새로운 브랜치를 생성하면서 동시에 checkout 하는 명령어.
    - $ git push -u origin remove-ipsum : 원격 리포지토리에 remove-ipsum 브랜치를 푸쉬하는 명령어
        ** 중요 : -u 옵션은 브랜치를 트랙킹 하는 것으로 pull, push할 때 브랜치를 설정하지 않아도 자동으로
                원격의 remove-ipsum 브랜치와 동기화 해준다.

### 70. Comparing and pull requests
    - 원격 리포지토리에서는 pull request로 두 브랜치를 합병했다.
    - remove-ipsum 브랜치에서 pull request를 클릭하면 master 브랜치와 병합이 가능한지 체크하고 병합한다.
    - 병합 후에 remove-ipsum 브랜치는 delete 한다.
    
### 71. Merging Locally
    - Merge : master 브랜치와 머지하기 위해서는 master 브랜치로 checkout 하여 현 상태가 master 브랜치가 되어야 한다.
    - $ git merge remove-ipsum : master 브랜치에 remove-ipsum 브랜치가 합병이 된다.
    - $ git branch -a : 로컬 리포지토리의 브랜치 리스트를 다음과 같이 확인할 수 있다. 
                        (원격 리포지토리에서 병합 이후에 remove-ipsum 브랜치는 삭제했다. 로컬에서도 해당 브랜치를 삭제해줘야 한다.)
![55](https://user-images.githubusercontent.com/26863285/46252114-62216500-c49f-11e8-982c-323f47c27a0f.png)                

                [위와 같이 remove-ipsum 브랜치가 삭제됨을 볼 수 있다. 하지만 원격 리포지토리의 참조는 남아있다.]
     
     
     
     - $ git fetch -p : 원격리포지토리와 로컬리포지토리를 동기화한다. 삭제된 브랜치가 있는지 체크한다. 
![default](https://user-images.githubusercontent.com/26863285/46252135-9d239880-c49f-11e8-90de-0e8a3a4ac409.png)
                             
                 [위와 같이 로컬에서 삭제된 브랜치의 원격 참조도 -p 명령어로 삭제됨을 확인할 수 있다.]


### 72. Locally switch to a Branch on Github
    - Github에서 update-readme 브랜치를 새로 생성한다. 그러면 현재 원격에는 update-readme 브랜치가 생성되고 로컬에는 현재 없는 상태이다.
    - $ git branch -a : 원격 리포지토리에 생성된 update-readme 브랜치를 확인 가능하다.
    - $ git fetch : 로컬리포지토리와 원격리포지토리를 탐색하여 비교한다.
    - $ git checkout update-readme : 이렇게 하면 원격에 리포지토리가 있는지 검색하여 로컬과 동일하게 브랜치를 만들어준다.
    
