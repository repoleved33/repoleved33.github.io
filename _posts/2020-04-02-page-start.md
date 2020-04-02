---
layout: post
title: Github.io Pages 블로그 시작하기
subtitle : 블로그를 시작하며
tags: [diary]
author: repoleved33
comments : True
---

학부 4년, 업무 2년에도 불구하고 스스로에게 '개발자'라는 이름을 붙이기엔 여전히 많이 부족하다는 생각이 들었다.
그래서 생각한 것이 개발 블로그 시작하기!

<br>

### github.io 선택 이유
찾아보니 tistory가 제일 흔하게 쓰이는 것 같은데,   

마크다운 언어를 배워보고 싶기도 했고 무엇보다도 직관적이고 깔끔한 UI에서 블로그를 작성하고 싶어서 github.io 페이지를 선택했다. 또 ruby나 jeykll 관련 공부가 더 필요하겠지만 원하는대로 커스텀 할 수 있다는 점도 장점으로 다가왔다.   

뭐, 쓰다가 다른 플랫폼으로 이전할 수도 있지 않을까?

<br>

### 2020 Plan

* <b>클라우드</b>    
 -- Azure 자격증 취득 (level ???)   
<br>
* <b>스프링</b>   
 -- [클라우드 네이티브 자바]
 -- Spring boot, IntelliJ 사용해보기   
<br>
* <b>알고리즘</b>   
 -- java/javascript 기본적인 문법은 찾아보지 않고도 작성할 수 있도록   
 -- [코딩 인터뷰 완전분석]   
 -- 백준, 프로그래머스, leetcode 등 활용 예정   
<br>
* <b>리액트</b>   
 -- [리액트 교과서]   
 -- [리액트를 다루는 기술] -> 코드 작성해보기   
<br>
* <b>M/L, D/L</b>   
 -- [머신러닝 도감]   
 -- [데이터 과학을 위한 통계]   
 -- python 문법 및 딥러닝 기초   

<br>

### github.io 프로젝트 시작하기
* 소스 clone
> `>`git clone https://github.com/repoleved33/repoleved33.github.io.git   
> `>`git config --global user.name "repoleved33"   
> `>`git config --global user.email "repoleved33@gmail.com"   
> `>`git config --list   

* 로컬 환경에서 테스트 (localhost:4000)
> `>`cd repoleved33.github.io   
> `>`bundle install   
> `>`bundle exec jekyll serve   

* commit
> `>`git add .   
> `>`git commit -m “[커멘트입력]”   
> `>`git push   

<br>

* * *
Jeykll template 출처 : [https://github.com/naye0ng](https://github.com/naye0ng)
