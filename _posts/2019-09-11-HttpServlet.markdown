---
layout: post
title: Web
date: 2019-09-12 00:16:02 +82
description: First HttpServlet
img: 
tags: [HttpServlet, JAVA]
author: Boyun
---

 
## HelloWorld Servlet 컴파일 및 실행하기
1. Java EE perspective / Java perspective
 - Java EE가 Web Application 만들 때 편한 환경 제공
2. Web Application 만들 때 WAS 설정 잊지 않기 
 - Target runtime에서 Tomcat 지정 해 주기 !

### Servlet ? URL 요청을 처리하는 프로그램
1. Eclipse는 보통 runtime으로 설정 된 WAS에 규칙의 URL로 서블릿을 실행하도록 설정해 줌
 - http://localhost:8080/{프로젝트이름}/{URL Mapping값}
2. response 객체 : 응답 할 정보들을 모아서 추상화해놓은 객체
 - response.setContentType() : 응답 결과가 무엇인지 브라우저에게 알려줘야 브라우저가 해석할 수 있음
 {% highlight java %}
protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		response.setContentType("text/html;charset=UTF-8");
	}

{% endhighlight %}