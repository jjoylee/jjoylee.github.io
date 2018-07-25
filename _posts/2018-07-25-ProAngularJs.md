---
layout: post
title: 2018-07-25-프로AngularJS
tags: [TIL]
---

대부분의 자바스크립트 메서드 호출은 동기적<br>
동기적 == 현재 명령이 완료되기 전까지 다음 명령을 실행하지 않는다.<br>

Ajax(Asynchronous JavaScript And Xml)<br>
Ajax 요청은 비동기적으로 일어나는 일반 HTTP요청(background에서 수행)<br>
AngularJS는 Promise를 사용해 비동기적 작업을 나타낸다.(비동기 처리에 사용되는 객체)<br>

------------------------------------------------------------------------------

Module : 어떻게 애플리케이션이 구동되어야 하는지 명시<br>
AngularJS 애플리케이션에서 최상위 레벨 컴포넌트<br>
역할1. AngularJS 애플리케이션을 HTML문서의 영역과 연계한다.<br>
역할2. 핵심 AngularJS 프레임워크 기능에 대한 게이트웨이 역할을 한다.<br>
역할3. AngularJS 애플리케이션에서 코드 및 컴포넌트를 정리하는데 도움을 준다.<br>

Module 객체에서 정의하는 메서드
- AngularJS 애플리케이션용 컴포넌트를 정의하는 메서드
- 컴포넌트를 쉽게 생성하게 해주는 메서드
- AngularJS 생명주기 관리를 도와주는 메서드

myApp.controller("dayCtrl", function($scope)) 
- 컨트롤러의 의존성 선언(필요로 하는 AngularJS 컴포넌트), $scope에 대한 의존성 선언