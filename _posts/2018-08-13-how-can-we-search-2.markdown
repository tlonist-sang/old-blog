---
layout: post
title:  "나는 어떻게 구글에서 자료를 찾을 수 있을까-2?"
date:   2018-08-13 00:45:22 +0900
categories: 네트워크
---
첫번째 포스팅에선 초월적 활자규약과 http에 관한 이야기를 잠깐 했다. 
궁금증이 사실 전혀 해소되지 않았다. 다음 행동으로 가보자. [같이 보면 좋은 링크](https://webhostinggeeks.com/guides/dns/
)

#2. https://www.google.com 입력하고 엔터를 친다. 
- 가장 먼저 브라우저가 www.google.com 의 진짜 IP 주소가 뭔지 알아내기 위해 캐시(cache)를 뒤져 DNS 기록을 확인한다. DNS는 Domain Name Server의 약자로, 인간친숙한 내비게이션을 위해 고안된 서버라고 할 수 있다. 매번 10.89.39.238:8080 을 치는 대신에 간단하게 www.google.com 이라고 치면 굉장히 삶이 편해지기 때문이다. 

- 브라우저 캐시에 없으면 OS cache를 본다. 그래도 없으면 router cache, 또 없으면 ISP (Internet Service Provider) cache를 참고한다. 만약 모든 단계에서 실패하면 ISP의 DNS에 직접 물어본다. 그렇게 해서 내가 문의한 자연어 URL에 해당하는 실제 IP를 알아낸다. 단계가 많아보이지만 굉장히 순식간에 일어남이 틀림없다. www.[아무말이나길게지어내보자].com 을 쳤을때 결과는 굉장히 빠르게 나온다. 

 ![img]({{ "/assets/img/DNS.png"|absolute_url}})

- DNS는 위의 그림처럼 재귀적으로 다른 DNS서버들을 호출하며 유저가 입력한 URL 값에 해당하는 실제 IP를 알아낸다. 결과적으로, 자연어 URL을 실제 https://www.google.com의 아이피 주소로 이동시키는 일이 그 다음에 일어난다. 

 ![img]({{ "/assets/img/tracert.png"|absolute_url}})

 ** 덤 **
cmd 창에서 tracert(trace route) google.com 을 쳐보면 흥미로운 결과가 나온다. 바로 해당 사이트의 실제 IP 주소가 나오는 것! 실제로 스샷에서 나온 주소로 들어가보니 google 메인 화면이 떴다. 





[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
