## Quick Install on Winows

### 1) Git for Windows
    - official Website : http://Git-SCM.com
    - Download for Windows
    - 설치시 디폴트로 설정하고 인스톨하기
    - 기호에 따라
      - Checkout as-is / Commit Unix-style  를 설정할 수 있다.
      - 필수는 아니다.
    - Minimal Configuration : 사용자 이름, 이메일
      - git config --global user.name "Your Name"
      - git config --global user.email "your@email.com"
 
 ### 2) NotePad++ 설치 : Git Bash에서 사용할 텍스트 에디터
     - Website : http://Notepad-Plus-Plus.org
     - Standard installer : 설치시 모든 것이 디폴트, Add shortcut to Desktop

### 3) NotePad++ 환경설정
    - Notepad 환경변수 설정 : D:\Program Files\Notepad++ 노트패드가 설치된 폴더를 PATH에 추가하기
    - notepad++ ~/.bash_profile 명령어 : Git Bash에서 이 명령어를 실행한다. 그리고 다음 명령어를 작성하고 저장한다.
      - alias npp='notepad++ -multiInst -nosession' 명령어 : 이 명령어를 입력하고 저장후 다시 Git을 시작한다.
    - git config --global core.editor "notepad++ -multiInst -nosession" 명령어 : Git의 디폴트 텍스트 에디터를 노트패드로 하는 명령어
    - git config --global -e : Notepad++가 디폴트 에디터로 설정되었는지 확인하는 명령어
    
### 4) P4Merge for Windows
    - 사용이유 : 머지를 할 때 편리하다. 커맨드라인으로 머지하는 것은 어렵다.
    - Website : https://www.perforce.com/downloads/visual-merge-tool
    - P4Merge 다운로드 : 운영체제에 맞는 exe 파일을 다운 받는다
    - 인스톨 파일 실행 : 오직 Merge and Diff Tool(P4Merge)만 선택해서 다운받기
    - git config --global diff.tool p4merge 명령어 입력
    - git config --global difftool.p4merge.path "C:/Program Files/Perforce/p4merge.exe"
    - git config --global difftool.prompt false 명령어
    - git config --global merge.tool p4merge 명령어
    - git config --global mergetool.p4merge.path "C:/Program Files/Perforce/p4merge.exe"
    - git config --global mergetool.prompt false
