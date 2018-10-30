# Git 명령어, Markdown 명령어

## Markdown 명령어로 작성

### Git, Markdown 순으로 작성

-----------
1.Git 명령어
-----------
*.git : 로컬 저장소
echo : vi편집기로 파일 생성 후 빠져나오는 것 까지 하는 명령어.
git init : .git 생성
add : unstaged 영역에서 staged영역으로 올리는 명령어
commit : 로컬 저장소에 저장하는 명령어.
-m : 메시지를 넣는 명령어
commit - m "메시지 내용"
remote add origin http:/ /github 주소  => 원격 저장소를 내 저장소와 연결 시키는 작업.
origin : remote에 있는 원격 저장소의 이름*

-----------
< 설정 >
-----------
*git config --global user.name "사용자명"
: 사용자명을 등록*

*git config --global user.email "이메일주소"
: 이메일 주소를 등록합니다.*

-----------
< option >
-----------
*git config --global color.ui "auto"
: 출력결과 색상 활성화하기
git config --global color.ui "off"
: 출력결과 색상 비활성하기*

-----------
< 초기화 >
-----------
*git init
: 내부 저장소 생성.*

-----------
< 내부 저장소 저장 : add & commit >
-----------
*- 수정된 파일 index로 이동*
 *1. git add <file명>  : 파일 1개씩 이동*

*2. git add . : 디렉토리 안의 수정된 모든 파일 이동*

===========
< index에 있는 내용 내부 저장소에 스냅샷으로 저장 > 스냅샷 : 변경된 부분만을 사진 찍듯이 저장하는 것.
===========
**git commit -m "this is commit message "**

-----------
< 상태 확인 : status >
-----------
*git status
: 현재 git 상태 확인*

*git reflog
: log 확인*

-----------
< HEAD상태로 이동 >
-----------
*git reset --soft HEAD~
: 바로 전 HEAD로 이동*

*git resert HEAD@{2} <file>*
 :2번 HEAD로 이동

*git reset HEAD < file >*

*git reset HEAD "파일명"
: 스테이지로 이동된 변경사항 되돌리기 . 즉 , unstage 하는 것
HEAD : 가장 마지막으로 commit 된 곳.*

**reset : 마지막 commit 한 시점으로 되돌리는 것.**

-----------
< remote & push >
-----------
- 원격 저장소에 설정
*git remote add < 원격 저장소 >  <저장소url >
ex) git remote add origin https:/ /github.com/name*

**- 원격 저장소 설정 확인 **
*git remote -v*

**- 원격 저장소에 저장(push)**
*git push <원격 저장소 > <branch>*

*ex) git push origin master*

-----------
< clone & pull >
-----------
**- 원격 저장소에서 복사본 가져오기**
*git clone <url>*

**- 원격 저장소에서 최신 변경사항 받아오기**
*git pull <원격 저장소 > <branch>*

*ex) git pull origin master*

-----------
< 가지치기 : branch >
-----------
*1. git branch
: 로컬 저장소의 branch 목록 보기
2. git branch -r
: 원격 저장소의 branch 목록 보기
3. git branch branch_name
: 새로운 branch 만들기
4. git checkout branch_name
: 작업 트리 이동
5. git merge branch_name
: 합치기 - merge
6. git branch -d branch_name
: merge된 branch 삭제*

-----------
< 가지 이동 : checkout >
-----------

**- commit log 보기**

*1. git reflog*

*2. git checkout (commit_id)*

*3. git checkout -b <name>*

**- branch 만들고 commit 상태 되돌리기 **

*1. git branch <name> (commit_id)*

*2. git checkout <name>*


-----------
pull : 가져오자마자 mix(가공) 시킨 느낌. 서버에서 바뀐 것이 있는지 확인하고 가져오기까지. 
fetch : 데이터를 가져와서 서버에서 바뀐것이 있는지 확인하는 것. 가져오는 것 까진 하지만 merge를 하지 않는 것.
-----------

*ex ) checkout을 통해서 3번 commit으로 이동해서 branch 생성.*



-----------
< 되돌리기 : reset >
-----------
*- commit log 보기*
*1. git reflog*

*- HEAD 상태로 이동
git reset --soft HEAD~
: 바로 전 HEAD로 이동*

*2. git reset HEAD@{2} <file>*
  : 2번 HEAD로 이동

*3. git reset HEAD <file>*
:  스테이지로 이동된 변경사항 되돌리기

*branch생성 후 수정.*

*master로 이동 후 *

[IT기초정리 # 07. GitHub연동/Git console명령어/Markdown|작성자 티메] (https://blog.naver.com/hunter8714/220811923681)


============
Markdown문법
============

-----------
1.#텍스트
-----------
*- #을 하나 쓰면 HTML의 <h1> 태그를,
   #을 두개 쓰면 <h2>의 태그를 의미한다.*

*- 즉, #은 하나에서 여섯개까지 쓸 수 있고, #이 늘어날 때마다 제목의 수준은 내려간다. (보통 글씨 크기가 작아진다. )*

-----------
< 리스트 >
-----------

*1. 번호없는 리스트
  문법 : -/+/* 텍스트*
*2. 번호 없는 리스트
  문법 : 숫자, 텍스트*

-----------
< 텍스트 강조 >
-----------
*1. 이탤릭
 문법 : *텍스트* , _텍스트_*

**2. 볼드체
문법 : **텍스트**, __텍스트__**

*하나는 이탤릭*, **두개는 볼드체**

3. 인용
문법 : > 텍스트

-----------
< 링크 >
-----------
1. 인라인 링크
문법 : [텍스트] (링크주소)
2. 참조 링크
문법 : [텍스트][참조명]
          [참조명]:링크주소

-----------
3. 이미지
-----------
문법 : ![텍스트](이미지링크)

-----------
< 소스 코드 >
-----------

*문법 : ` ` ` 언어
          코드
          ` ` `
 - 언어에는 소스코드에 해당되는 언어를 넣어준다. objective-c, python, sh, java 등..
 - 코드 내용의 문법에 맞게 색상이 자동 추가된다.*

[https://blog.naver.com/hunter8714/220811923681](https://blog.naver.com/hunter8714/220811923681)
