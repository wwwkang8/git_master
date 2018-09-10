##Section 5. Advanced_Beyond_Basics

### 29. Comparing Differences
  - $ git diff 0785452 HEAD : 커밋 0785452와 HEAD(브랜치의 마지막 커밋)과의 차이를 비교할 수 있다.
  - $ git difftool 0785452 HEAD : P4merge가 뜨면서 diff가 있는 모든 파일들을 띄워준다.
  - 파일을 변경했는데 어떤 부분이 변경되었는지 모를 때
    - README.md 파일 변경했을 떄
    - $ git diff : 가장 최근 변경된 파일과 HEAD를 비교해서 보여준다.
    
### 30. Branching and Merge Types
    [Branch]
      - Branch = Timeline of Commits
      - Branch Names are labels
      - 브랜치는
    [Type of Merge]
      - Fast forward Merge : 아무런 추가적인 작업이 부모 브랜치(master)에 없을 때 바로 병합 가능.
        - Non-fast-forward : 부모 브랜치에 작업이 되어있을 때. (해결 : pull 받고 커밋 후 다시 푸쉬)
      - Automatic merge : 부모 브랜치와 아무런 충돌이 없을 때 2개의 브랜치가 합쳐진다.
![20180910_093617](https://user-images.githubusercontent.com/26863285/45270882-0df91580-b4dd-11e8-8946-bdc24286dc5f.png)
      - Manual merge : 개발자가 스스로 충돌을 해결하고 머지하는 것

### 31. 
