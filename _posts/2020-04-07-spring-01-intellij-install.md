---
layout: post
title: IntelliJ community 버전에서 Spring Boot 시작하기(1)
subtitle : 개발환경 구성하기, maven과 gradle
tags: [Spring, IntelliJ, Backend]
author: repoleved33
comments : True
---




<br>

윈도우 사용 시절에 STS는 너무 무거웠던 기억이 있어서 다른 IDE를 고민하다가 한번도 써보지 않은 IntelliJ에서 시작하기로 했다. 
<br>
- 설치환경: macOS Catalina 10.15.3(업데이트 해야하는데..)
- IDE: IntelliJ 2019.3.4
- Java: JDK 11
<br>
<br>

### Spring Boot 프로젝트 개발환경 구성
##### JDK 설치   
스프링부트 5.X부터는 현재 LTS 버전인 Java SE 11를 지원한다.   
[>JDK 11.0.6 다운로드<](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)   

##### IntelliJ 공식 홈페이지에서 다운로드(Community 무료버전)   
[>인텔리제이 공식 홈페이지<](https://www.jetbrains.com/idea/)   

##### Spring Initializr 플러그인 관련   
IntelliJ community 버전에서는 Spring Initializr 플러그인을 기본으로 지원하지 않는다고 한다.   
Spring 프로젝트를 시작하는 방법으로 두 가지 정도가 있다.   
<br>
1. Empty Project에 모듈 설정을 통해 프로젝트 설정   
2. spring.io에서 제공하는 형태를 zip으로 다운받아 open   

<br>
스프링부트에 익숙하지 않기 때문에 두번째 방법으로 진행하기로!   
Project(Gradle/Maven), Language(Java/Kotlin/Groovy), 버전 및 기본정보를 선택하면 된다.   

[>Spring 프로젝트 생성 바로가기<](https://start.spring.io/#!type=gradle-project)   

<br>

* * *

<br>

### Maven과 Gradle
프로젝트에 필요한 모든 Dependency(종속성)를 리스트 형태로 알려 관리해주는 build tool이다.   
- 라이브러리 의존성 관리, 라이브러리 추가 및 버전 동기화를 자동으로 관리 
- 빌드 자동화 툴로, 자바 소스를 compile하고 pacakge해서 deploy하는 일을 자동화해주는 역할 _~~(+4.17 추가)~~_

##### Maven
- pom.xml을 사용해서 익숙하고 정형화된 설정이 가능하나 서로 종속할 경우 xml이 복잡해짐
- 개발 가이드라인 제공
- 계층적인 데이터 표현에 좋음

##### Gradle
- Ant와 Maven의 장점을 모아 출시, 설정 주입 방식
- Android OS 공식 build tool
- JVM 언어인 Groovy가 사용되어, 자바와 유사하기 때문에 배우기 쉬움  
- 간단한 빌드 스크립트 작성으로 더 빠르고 간결함
- 멀티 프로젝트에 유리함   
<br>
빠른속도와 간편함만으로도 Gradle을 사용할 이유가 충분하다고 판단했다.
  

<br>

* * *
참고자료   
[스프링 Empty Project 모듈 설정 관련](https://www.bsidesoft.com/?p=6926)   
[spring.io 프로젝트 제공 관련](https://yuhe-dogspaw.tistory.com/m/198?category=319589)   
[spring.io 프로젝트 제공 관련2](https://steps-for-developer.tistory.com/entry/Intellij로-SpringBoot-게시판-만들기-1)   
[Maven vs Gradle](https://bkim.tistory.com/13)   




