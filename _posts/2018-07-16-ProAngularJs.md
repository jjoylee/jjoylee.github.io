---
layout: post
title: 2018-07-16-프로AngularJS
tags: [TIL]
---

AngularJS - HTML 확장(커스텀 엘리먼트, 어트리뷰트, 클래스, 주석)

MVC 패턴 - 관심사의 분리<br>
           Application의 Model은 Business 및 Presentation Logic 과 분리된다.<br>
           data, data를 처리하는 logic, data를 보여주는 HTML Element를 분리해야 한다.

Model - 사용자가 사용할 data가 들어있다.<br>
        유형 1 : View Model <br>
          - Controller에서 View로 전달된 data.<br>
        유형 2 : Domain Model<br>
          - Business domain 내 data, 작업, 변형<br>
            데이터를 생성, 정렬. 조작하는데 필요한 규칙이 들어있다.(Model Logic)

Controller - Data Model과 View를 연결<br>
             Business Domain Logic을 Scope에 추가<br>

HTTP 방식에 대한 응답으로 수행하는 주요 작업<br>
GET : URL을 통해 지정한 데이터를 조회한다.<br>
PUT : URL을 통해 지정한 데이터를 업데이트한다.<br>
POST : 주로 form 데이터 값을 데이터 피드로 사용해 새 데이터 객체를 생성한다.<br>
DELETE : URL을 통해 지정한 데이터를 삭제한다.