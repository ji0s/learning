# learning
코린이의 하루 240503

미루다 영원히 미룰뻔한 git hub 만들었다.
오늘 visual basic 이랑 처음 연동했다.

연동부터 삐그덕, 앞으로 잘할 수 있을까.

* Github으로 TIL 시작하기 (Doing님 가이드 발췌)

1. 레포지토리 생성
자신의 github계정을 만들고 Respositories의 New버튼을 클릭한다.
리드미 파일을 꼭 추가하자! -> 아마 이걸해야 연동되는듯? 잘모르겠다.
 
2. 레포지토리 생성 확인

바로 여기서 Add file을 만들어쓰고 README.md옆에 연필버튼을 사용해서 작성하면된다.
근데 이렇게 사용하게되면 한 파일을 수정할때마다 1커밋을 해야했다.
그니까 spring폴더에 controller이라는 글을 작성하고 1커밋하고, 다시 README.md에서 controller글의 링크를 걸면서 또 다른 1커밋을 해야했다. 의미없는 커밋이 늘어나는 것같아서 이 방법이 아닌 다른 방법을 생각해보았다.
 

**git hub와 VB 연동
블로그보고 brew 써야하는줄알고 깔았는데 돌아보니 크게 필요없는듯하다.
아니면 깔아서 지금 되는건가?

1. visual basic 을 깐다.
2. 연결할 폴더를 미리 하나 새로만든다.

1) 맨위 terninal 을 열어 new terminal 을 클릭. 아래 코드 입력창아래 터미널 창이뜬다. 
2) git add . 하고 엔터 '.' 전에 띄어쓰기 한번, 뒤에 . 은 변경사항이 있는 파일 전부를 대상으로 하겠다는 뜻이다. 특정파일만 하고 싶다면 특정파일 이름을 쓰면된다. 

3) git commit -m "ㅇㅇㅇ변경 (커밋 메세지: 변경된 내용에대한 간략한 설명)"

4) git push -u origin main (저장한 것 내보내기)
기본으로 origin 으로 설정되어있다고 함.

- [git remote -v]로 확인해보면 정상적으로 연결된거 확인가능.
- git --version 으로 버전 확인가능. 

ㄹㄹ
1.git init > .git 이라는 하위 디렉토리 생성. 저장소에 필요한 뼈대파일있음.
2. git add . 로 > 버전 관리를 새롭게 추적할 파일을 추가할 때 사용. Workspace 에 있는 파일 중 내용 변경이 있는 모든 파일 선택하는 명령어, 만약 추가할 파일을 선택하고 싶을때는 git add파일이름.확장자 이렇게 입력.
#Example
git add NewFile.txt

3. git status > 상태 확인
4. git commit > commit 한 시점의 내용을 스냅샷으로 저장하고, 해당 스냅샷에 대한 commit 객체를 만듬. 
5. git commit -m"comment" > -m은 commit 메세지를 파라미터로 넘기는 것인데, -m 를 하나만 쓰면 제목만 -m 두개 쓰면 제목과 Description 이 된다. 
#Example
git commit -m "Reversion.0" > 제목만
git commit -m "Reversion.0" -m"add code" > 제목과 설명
6. github 에서 repository name 으로 프로젝트 만들고 (이름 동일하면좋음 헷갈림 방지) Creat Repository 로 github 저장소 만들기
7. git remote add origin https주소 를 터미널에 입력
https 주소는 local > SSH 주소를 넣어야함.
8. git push origin main = git push > Github 저장소에 로컬 디렉토리 프로젝트의 파일 추가된 것을 볼 수 있다.

별첨
커밋 메세지 가이드: README_ko-KR.md

문서작성 완료 후,파일을 수정한 후, 새 터미널 열기
1. git pull 원격 저장소의 데이터를 로컬 저장소에 최신화. 건너뛰면 충돌 발생. already up to date 라고 뜨면 이미 최신화
2. git status 로 로컬 작업 공간의 상태확인
3. git diff 로 수정된 파일의 내용확인
4. git add . > . 은 모든 파일을 의미. 작업사항을 스테이지에 추가
5. git ad README.md > 모든 파일을 스테이지에 올리고 싶지 않은 경우에는 파일명으로 스테이지에 추가.
6. git status 로 상태확인 
your branch is up to date with 'origin/main' > ok
7. git commit 으로 커밋 git commit -m "메세지"
8. git status 로 상태확인 > 우너격저장소에 push 할수 있는 commit 있는 것 확인
9. git push 로 commit 을 원격 저장소로 올림.
만일 작업 중에 원격 저장소에 누군가가 올렸을 경우 최신화가 되지 않았기 때문에 git pull 과정을 거쳐야할 수 도 있다. 

끗