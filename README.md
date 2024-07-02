<a name="top"></a>

# mbcac_project
## 팀 프로젝트 안내

* 주제 : 열심히 하자
* 기간 : 3달
  + 1달:분석
  + 1달:설계
  + 1달:구현
    - 1주:로그인
    - 2주:게시판
    - 3주:뉴스
<a name="code1">code1</a>
## 아래의 코드를 참고하세요
```jsp
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<%@ page import="net.mbcac.board.BoardVO" %>
<%@ page import="net.mbcac.board.BoardDAO" %>

<%@taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>

<jsp:useBean id="dao" class="net.mbcac.board.BoardDAO" />
<jsp:useBean id="b" class="net.mbcac.board.BoardVO" >
	
	<jsp:setProperty name="b" property="*" />

</jsp:useBean>

<c:set var="bnum" value="${dao.addBnum(b)}"></c:set>
{"added":${num>0},"bnum":${bnum}}
```
[github마크다운으로 색상설정하기](https://gist.github.com/luigiMinardi/4574708d404cdf4fe0da7ac6fe2314db)




<a name="code2">code2</a> [go to top](#top)
Github
팀 프로젝트 코드 공유
https://github.com 
 -Remote Repository(프로젝트 원격 저장소)
 -개인 홈페이지
 -git: 원격저장소에 대한 입출력을 위한 클라이언트 툴, 내 컴퓨터에서 commnand line툴을 이용하여 로컬 저장소를 만들고 관리하는 툴을 제공(git명령어 필요)
 -git툴을 이용하여 원격 저장소에 있는 프로젝트를 관리하려면 git명령어가 필요하다
 -git은 cli(Command Line Interface)프로그램과 같은 모양
 -main(master) branch, 다른 branch로 나누어 프로젝트를 분리 저장 관리가 가능하다
 -로컬시스템에는 로컬저장소(Local Repository)

-작업 절차:
	로컬 저장소에 프로젝트 생성 
	> 원격 저장소를 미리 생성(github.com)사이트에서 원격 저장소 생성 
	> 원격 저장소에 저장된 프로젝트를 개발팀원들이 clone하여 
	  로컬 저장소에 프로젝트 생성
	> 팀원들은 각자의 업무를 코드로 작성
	> Staging(git명령어로 ‘add’) 
	> Commit(작업 명령의 history생성, 작업 마디 단위로 후퇴하여 취소할 수 있음) 
	> push : 작업물의 타당함을 보고 관리자가 로직을 합침(서버로)


 
<a name="code3">code3</a> [go to top](#top)
 -git설치
1. cmd에 ‘git —version’을 검색해서 실행되는지 확인
2. https://git-scm.com 에서 우측 중앙의 ‘Download for Windows’버튼 클릭
*SCM(Source Code Management)
3. 윈도우에 git과 관련된 id와 password가 있을 수 있음
   - 윈도우 자격증명 확인
	1. 윈도우 자격증명 관리자 > Windows 자격증명 > github 자격증명 삭제
4. 64-bit git for Windows Setup  클릭 > 설치
5. cmd실행하여 ‘git —version’ 검색 > 버전 확인
6. git설치유지 명령
	- git config —global user.name “아이디”
	- git config —global user.email“이메일
	- 작성 내용 확인 명령어 : git config —list



<a name="code4">code4</a> [go to top](#top)
 - 리파짓토리 만들기
1. 우측 상단 프로필 클릭
2. ‘New Repository’
3. ‘New’클릭
4. Repository Name입력, public/private선택, Description입력(선택), Add a ReadME file 선택 > Creat Repository
5. README는 텍스트파일이므로 자유롭게 편집

 -리파짓토리 관리
1. 삭제 : 상단 메뉴의 Settings > 페이지 맨 하단의 Delete this repository
2. 리파짓토리는 하나의 디렉토리처럼 관리됨
3. 리파짓토리 아래 파일 추가 : 중앙 우측 상단에 ‘+’버튼 > 새파일생성/로컬파일업로드
	> 새 파일 생성 : 파일이름에 확장자명까지 입력 > 내용입력 > ‘Commint changes..’
4. 디렉토리 생성 : 메뉴는 따로 없음, 파일 생성방식으로 시작> 파일이름에 ‘/’이용하여 경로를 만들면 자동으로 생성
5. 중앙 우측에 ‘<>Code’버튼 : 
	- 주소 : 이용자가 local에서 써야할 git명령어, 통신할 때 리파짓토리 주소로 사용됨 
	- 명령프롬프트에서 로칼 디렉토리 생성 
		> 지정할 파일로 이동
		> ‘git init’ 
		> 메시지‘Initialized empty Git repository in C:/git_demo/.git/’ 확인
		> 파일탐색기에서 숨긴항목 표시
		> ‘.git’ 폴더 확인 
		git과 관련된 모든 항목이 저장됨
 -README파일 : html css이 사용되며 추가로 마크다운문법이 허용됨
	웹상에 표시할 문서를 html문서를 작성할 수 있음
	-파일명 : README.md (마크다운문서, 텍스트 파일)
	-웹브라우저에서 읽을 수 있도록 html문서로 바꾸는 기능
	-우측 상단의 commit changes.. 버튼 > 변경내역(history)으로 저장되어 롤백가능
	-main branch가 최종 배포판이 되므로 병합여부 선택하기
	-링크만들기 : 웹주소를 넣기


<a name="code5">code5</a> [go to top](#top)
 -마크다운 문법
# : jsp에서 <h1>태그와 같은 기능
## : <h2>태그와 같은 기능
*/+/- : 목록 만들기 > 특수문자를 사용하면 하위항목으로 인지
``` + 언어이름 : 코드 구현, 코드가 끝날 때 마찬가지로 ```
인라인스타일 : $\color{#ff0000}{\textsf{색상설정}}$
https://gist.github.com/luigiMinardi/4574708d404cdf4fe0da7ac6fe2314db
텍스트에 링크붙이기 : [텍스트](링크할 주소)



<a name="code6">code6</a> [go to top](#top)
