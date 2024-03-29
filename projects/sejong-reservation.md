---
title: Sejong Reservation
layout: project
type: web
image: sejong-reservation.png
short: <b>&nbsp;학교 내 회의실 예약을 위한 웹서비스</b><br>
desc: |
   <b>&nbsp;학교 내 회의실 예약을 위한 웹서비스</b><br>
   <ul>
   <li>수기로 이루어지던 회의실 예약 방식을 편리하게 만들기 위해 제작했다.</li>
   <li>자주 다운되거나 오버로드 되던 기존의 학교 시스템을 개선하기 위해 수평 스케일링이 가능한 <b>MSA 구조</b>로 설계했다.</li>
   <li>학교에서 실제로 사용할 시스템이기에, 관리와 운영의 편의를 위해서 <b>Docker Swarm</b>을 사용해 디플로이 했다.</li>
   <li>추후 업데이트를 쉽게 반영하기 위해 Github Actions를 사용해 <b>CI/CD 파이프라인</b>을 도입했다.</li>
   <li><b>회원제</b>로 운영이 되며 회원등급별로 페이지별 권한과 관리 기능을 다르게 하여 제작었다.</li>
   <li>Vue를 사용한 반응형 웹페이지를 만들었다.</li>
   </ul>
categories: html css js vue microservice flask flask-restx mariadb github-actions CI/CD docker docker-compose docker-swarm 
repo: https://github.com/iwakura1ain/sejong-reservation
live: https://sejong-LoadB-vkR3OU14tbdc-cfac865726bae2d2.elb.ap-southeast-2.amazonaws.com
---


# 개요

{% include desc.html %}
{% include stack.html %}


## 링크

-   **LIVE** : <a href="{{ site.baseurl }}/redirect/sejong-reservation/">{{ site.baseurl }}/redirect/sejong-reservation/</a>
-   **GITHUB** : <a href="<https://github.com/iwakura1ain/sejong-reservation>"><https://github.com/iwakura1ain/sejong-reservation></a>


## 인원과 역할

-   **안창언** : 팀장, 시스템/스키마 설계, 백엔드, CI/CD
-   한수현: 백엔드, 도큐멘테이션
-   장호진: 백엔드, API 설계
-   이원진: 프론트엔드, UI/UX 디자인, API 설계


# 제한사항


## 서비스별 데이터 독립화

-   SqlAlchemy ORM으로 개발을 진행했으나, 데이터 스키마는 한곳에서 관리를 하는 것이 옳다고 생각했다.
    
        그러나 ORM을 사용하게 되면 모델을 개별적으로 정의해야 되는 문제점이 발생했다.


### 해결

-   SqlAlchemy Core를 사용해 **스키마를 각 서비스별로 reflect해 모델 정의 없이 사용** 하는 기능을 만들었다.
-   **모든 서비스 아래로 상속** 시켜 프로젝트 전체에서 사용했다.
    
    <br>


## 초기 통합 테스팅 시 브랜치 관리

-   서비스별로 브랜치를 따로 관리하여 개발 진행했다.
-   통합과정에서 머지를 먼저 하지 않고 각 브랜치별 도커 컨테이너를 생성하여 테스팅을 시도했다. 
    
        팀원간 서비스별 버전이 엇갈리는 문제점이 발생했다.


### 해결

-   통합 테스팅 전에 머지를 먼저 하여 **통일된 테스팅 버전을 만드는 것** 이 중요하다는 것을 깨닳았다.


# 프로젝트


## MSA 구조 기반의 시스템 설계

-   **각 서비스간 REST** 로 통신
-   **Docker Swarm** 로 서비스별 load balancing/recovery 가능해야 함
-   서비스별 데이터 액세스는 분리, 그러나 **데이터 스키마는 중앙 관리**

![img](./sejong-reservation-architecture.png)


## CI/CD 파이프라인 구현

-   **Github Actions** 사용해 개인 컴퓨터에 디플로이

![img](./sejong-reservation-cicd.png)


## Reactive한 SPA 기반 UI

-   **Vue** 를 사용한 프론트엔드 개발
-   PC, 모바일 화면 지원

![img](./sejong-reservation-ui.png)


## 도큐멘테이션 생성

-   **Postman** 과 **readthedocs** 사용

![img](./sejong-reservation-doc.png)
