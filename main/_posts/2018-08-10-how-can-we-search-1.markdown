---
layout: post
title:  "How can I see stuffs on the internet? - 1(revised)"
date:   2018-08-05 00:45:22 +0900
img: google1.png
categories: Network
comments: true
---
reference: HTTP the definitive Guide

How can I search stuffs on Google? How is it possible to watch videos on Youtube?
About a year ago I tried to answer this question with my own effort, but wasn't so successful. Now that I've gained more knowledge of how it works, I want to start a series of postings that arranges my understanding on how web works in general. 

To be more specific, this series of posting will trace and study the following user scenario.

1. Run an internet browser, go to Google.com (I'm using Chrome Version 78.0.3904.108)
[![img]({{ "/assets/img/hcws5.png"|absolute_url}})]({{ "/assets/img/hcws5.png"|absolute_url}})

2. Type Amazon in the search box.
[![img]({{ "/assets/img/hcws4.png"|absolute_url}})]({{ "/assets/img/hcws4.png"|absolute_url}})

3. Click Amazon, and go into Amazon website.
[![img]({{ "/assets/img/hcws3.png"|absolute_url}})]({{ "/assets/img/hcws3.png"|absolute_url}})\
<br>
4. Type Borges in the search box.
[![img]({{ "/assets/img/hcws2.png"|absolute_url}})]({{ "/assets/img/hcws2.png"|absolute_url}})
<br>
5. Click 'collected Fiction'
[![img]({{ "/assets/img/hcws1.png"|absolute_url}})]({{ "/assets/img/hcws1.png"|absolute_url}})

#1.	인터넷 브라우저를 실행한다. (네트워크의 애플리케이션 계층)
-	웹브라우저를 실행하면, 애플리케이션이 시작되어 메모리에 올라가고, 프로세스로 간주되어 처리되기 시작한다. (이 과정은 시스템 프로그래밍 공부하게..되면 복습해보자) 애플리케이션 계층은 이 프로그램이 다른 장치에 로딩된 애플리케이션/서비스와 데이터를 교환하는데 있어 일관된 룰을 정립해준다. 한마디로 최상위 애플리케이션들이 어떤 약속으로 데이터를 교환할 것인가를 정해주는 것이다. 
 
 ![img]({{ "/assets/img/google1.png" | absolute_url }})
 
-	브라우저를 키면 기본으로 설정되어 있는 주소창의 https://www.google.com 의 https가 바로 이 애플리케이션 계층의 프로토콜이다. 초월적 활자 이동 규약이라는 뜻의 hyper text transfer protocol 은 말 그대로 이 텍스트에서 저 텍스트로 링크를 통한 널뛰기가 가능하다는 뜻이다. 

-	그럼 [초월적 활자 이동 규약]://www.google.com 은 어떻게 나에게 구글의 메인 화면을 띄워주는 걸까? 질문은 꼬리에 꼬리를 문다. [바로 이런것이다](http://tlonist.github.io/jekyll/update/2018/08/05/how-can-we-search-2.html)

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
