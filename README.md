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
