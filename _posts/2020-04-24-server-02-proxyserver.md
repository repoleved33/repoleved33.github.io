---
layout: post
title: Proxy sever
subtitle : foward proxy, reverse proxy, open proxy
tags: [Server]
author: repoleved33
comments : True
---


<br>
<br>

### forward proxy

프록시 서버를 클라이언트 호스트들과 웹 서버 사이에 위치시키는 방법     
클라이언트가 웹 서비스에 리소스를 요청하면, 사용자 PC가 직접 연결하는 게 아닌 forward proxy 서버가 요청을 받아 처리하여 결과를 클라이언트에 전달(forward) 해줌   
- 캐싱 제공
- 정해진 사이트만 연결할 수 있는 웹 사용환경 제공 : 기업 환경에 적합
- 비용 저렴
<br>


### reverse proxy

프록시 서버를 인터넷/인트라넷 리소스, 즉 서버 바로 앞단 frontend에 위치시키는 방법   
forward proxy와 구성 배치는 같지만 같은 서버 내에 다른 서비스 처리를 하는 곳으로 보내진다는 점이 다르다.   
보통의 기업 네트워크 환경에서는 DMZ라고 부르는 내부/외부 네트워크 사이의 구간에 reverse proxy 서버를 두고 실제 서비스는 내부망에 위치시킨 후 서비스한다.   
DMZ는 방화벽에 의해 보호되지 않는 영역이기 때문에 이 구간에 WAS를 둔다면 해킹을 당할 경우 DB에 직접 접근할 수 있기 때문에 보안 측면에서 문제가 될 수 있다.   
- 실제 서비스 서버는 내부망에 두고 프록시 서버만 내부와 통신하도록 하여 보안을 높임
- 프록시를 클러스터로 구성해놓으면 가용성 높이고 유연하게 확장할 수 있음
- load balancing 처리가능

일반적인 web(apache,nginx)-WAS(Tomcat) 분리 형태에서 나타나며, web이 reverse proxy라고 보면 된다.   
<br>

### open proxy

일반적인 인터넷 접속을 하기 위한 프록시로 IP 추적을 방지하거나 우회해서 접속하는 기능을 수핼할 수 있다.   


<br>
<br>
s
* * *

참고자료   
<https://www.lesstif.com/system-admin/forward-proxy-reverse-proxy-21430345.html>   
<https://cornswrold.tistory.com/404>   
<https://interconnection.tistory.com/27>