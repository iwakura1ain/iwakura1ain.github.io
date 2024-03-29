---
title: Fuzzit Web Scanner
layout: project
type: cli
desc: 웹서비스가 Injection 또는 Brute Force 공격에 취약한지 검사하는 CLI 보안 프로그램
image: fuzzit-help.png
short: <b>웹서비스가 Injection 또는 Brute Force 공격에 취약한지 검사하는 CLI 보안 프로그램</b><br>
desc: |
   <b>웹서비스가 Injection 또는 Brute Force 공격에 취약한지 검사하는 CLI 보안 프로그램</b><br>
   <ul>
   <li>CTF 보안 문제를 풀면서 웹서비스의 <b>취약점 탐지를 자동화하는 시스템</b>이 있으면 편리할 것 같아서 제작했다.</li>
   <li>GET, POST, COOKIE 인젝션 공격과 URL 스캔 기능을 만들었다.</li>
   <li><b>공격 패턴 자동 생성</b>과 <b>비동기적인 공격 탐지</b> 또한 가능하다.</li>
   </ul>
categories: cli python multithreading scanner injection brute-force cybersecurity 
repo: https://github.com/iwakura1ain/Fuzzit-Web-Scanner
---


# 개요

{% include desc.html %}
{% include stack.html %}


## 링크

-   **GITHUB** : <a href="<https://github.com/iwakura1ain/Fuzzit-Web-Scanner>"><https://github.com/iwakura1ain/Fuzzit-Web-Scanner></a>


## 인원과 역할

-   개인프로젝트


# 프로젝트


## 다양한 인젝션 공격 지원

-   일반 **Brute Force** 공격
-   **GET 메서드** 의 url 파라미터
-   **POST 메서드** 의 form 데이터
-   **COOKIE** 데이터
-   **URL 존재** 하는지

![img](./fuzzit-help.png)


## 서버로 보내는 데이터 중 공격에 취약한 부분이 있는지 검사

-   일반 **Brute Force 공격** 실행

![img](./fuzzit-scan.png)

-   Escape Character와 공격 패턴을 조합해 wordlist로 **Injection 공격** 실행

![img](./fuzzit-scan2.png)


## 사용할 인젝션 wordlist와 취약점 탐지 ruleset를 정의하여 사용

-   웹서비스에 보내질 **공격 패턴** 을 json 룰셋으로 생성
-   공격이 성공했는지 **탐지 패턴** 을 json 룰셋으로 생성
-   이때, curl과 같은 비동기적인 공격 패턴도 감지할 수 있는 기능 추가

![img](./fuzzit-ruleset.png)
