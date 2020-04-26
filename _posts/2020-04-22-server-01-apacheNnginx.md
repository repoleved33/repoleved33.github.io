---
layout: post
title: Apache vs Nginx 웹서버
subtitle : apache nginx 웹서버 비교하기
tags: [Sever]
author: repoleved33
comments : True
---




<br>

프론트 게이트웨이로 nginx를 사용하는데, 웹서버인 nginx에 대해 아는 바가 없어 찾아보았다.   
그동안 apache만 사용해왔기 때문에 어떤 차이가 있는지 알아보자.   
<br>
<br>

### apache
prefork로 구성. 최대 process의 갯수를 미리 정의해 놓고 어떠한 type의 request가 들어오든지 각각을 처리하기 위해 개별 process가 대응한다는 의미이다.   
(이때 최대 process 갯수 이상의 request가 동시에 들어오는 경우 해당 갯수를 넘어가는 요청은 reject된다.)   
즉, 요청 유형이 정적인 txt, png 형태 또는 server-side에서 처리하는 php 형태의 request 모두 별도 프로세스가 동작한다.   
그렇게 되면 비교적 간단한 정적 request 처리에도 필요 이상으로 많은 리소스가 사용되기 때문에 오버헤드가 발생한다.   
<br>

### nginx 
high performance & high concurrency & low resource usage 가 특징.   
동시에 최대 10,000건의 concurrnet connections까지 처리할 수 있도록 개발되었다.   
각각의 request를 하나의 nginx machine이 비동기 방식으로 처리한다.   
php와 같이 server-side 처리가 필요한 요청은 server process에서 처리된 뒤 nginx의 reverse proxy를 사용해 결과값을 전달한다.   
반면에 png/txt와 같은 정적 요청은 nginx machine에서 즉시 전달하기 때문에 리소스의 낭비가 줄어든다.   
따라서 자원을 효율적으로 필요한 곳에서 사용할 수 있게 되어, apache 웹 서버의 성능 문제를 어느정도 해소했다고 볼 수 있다.   

<br>
<br>

 * * *
 
 참고자료   
[apache와 nginx](https://velog.io/@minholee_93/Nginx-Overview-Install/ )