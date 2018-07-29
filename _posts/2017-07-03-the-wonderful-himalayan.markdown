---
layout: post
title: "My first question: How can we search stuffs online?"
img: searchengine.png # Add image post (optional)
date: 2018-07-29 10:00:00 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
tag: [IT, Computer Science, Developer]
---
How can we search stuffs online?
주말 회로
나는 어떻게 구글에서 자료를 찾을 수 있을까?
왠지 예전에 공부했던 네트워크 계층구조를 훑는 시간이 될 꺼 같다. 한번 쭉 훑어보면서 최대한 실제 물건들을 보고 느껴가며 정리해보자. 

1.	브라우저 (Chrome, Internet Explorer, Firefox)등을 켠다. 웹 브라우저란 뭘까?
웹 브라우저의 목표는 유저의 디바이스에 정보 자료를 1)가져와서 2)보여주는 것. http, https와 같은 통신 프로토콜을 사용할 때는 file://로 시작할 때는 사용자 컴퓨터(로컬)에서 가져온 정보를 나타낸다. 웹 페이지를 가져와서는 브라우저의 렌터링 엔진이 유저의 디바이스에 그것을 보여준다. 즉 간단하게 얘기해선 특정 프로토콜을 사용하여 웹페이지를 가져오고 그것을 렌더링하여 보여주는 역할을 하는 소프트웨어라는 것.

2.	www.google.com 이라는 검색엔진이 활성화되어 보여진다. https://www.google.com 이란 무엇이며, 정확히 어떤 원리로 창이 뜨는 것일까? 예를들어 myprotocol://give me sunmi pic 은 왜 안되는 걸까? (어디에서 막히는 걸까?)

3.	검색엔진이 하는 역할이 정확히 무엇이며, 나도 검색엔진을 만들 수 있을까? 
검색엔진은 1)크롤링, 2)인덱싱, 3)리트리벌이 주요 하는 일이라고 할 수 있다. 
1) 크롤링: 인터넷을 통해 연결된 수많은 웹페이지들을 방문하며 그것을 큐(queue)에 넣어 리턴하는 일. 어떤 페이지들은 크롤링을 허용하지 않으며 
2) 인덱싱: 크롤링 된 데이터가 처리되어 데이터베이스화 되는 것. 즉 크롤링을 통해 돌아다니며 수집한 데이터를 모아서 리스트화하여 가지고 있는 것. 구글 데이터 센터는 그럼 그 모든 데이터가 들어있는 곳?! 그렇다면 결과적으로 구글 데이터 센터는 크롤링을 허용한 모든 페이지들을 긁어와서 저장해놓고 있다는 뜻?!!
3) 리트리벌(가져오기)과 랭킹 : 리트리벌은 검색 엔진이 나의 검색 쿼리를 수행하여 가장 연관있는 페이지들을 보여주는 것. 서치엔진마다 결과가 다른 이유기도 하다. 랭킹 알고리즘은 수십억개의 다른 페이지들과 나의 쿼리를 비교하여 각각의 연관성에 따라 순위를 매기는 일을 한다. 
