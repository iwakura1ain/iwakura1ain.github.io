---
title: Financiar
layout: project
type: web
image: financiar.png
desc: |
   <b>과거 주식 데이터로 모의 투자를 하는 웹서비스</b><br>
   <ul>
   <li>간편하게 투자전략을 검증 할 수 있는 서비스를 만들고 싶어 제작했다.</li>
   <li>사용자가 S&P500 주식을 검색하여 <b>과거 주가를 조회</b>하거나 해당 주식을 사용하여 <b>모의 투자</b>를 하는 웹서비스이다.</li>
   <li>종목은 분야별, 이름별 <b>검색이 가능</b>하며 주가 자체는 Yahoo Finance를 크롤링하여 <b>redis에 캐싱</b> 후 제공된다.</li>
   <li>무한스크롤이 가능한 종목 페이지와 상호작용이 풍부한 <b>인터랙티브 그래프</b>로 사용자의 참여를 유도한다.</li>
   </ul>
categories: finance html css js react django drf pandas selenium redis mariadb docker docker-compose
repo: https://github.com/iwakura1ain/Financiar
live: http://financ-loadb-h39ibtrlr5el-32ad447233d6e4ff.elb.ap-southeast-2.amazonaws.com:5173/
---


# 개요

{% include desc.html %}
{% include stack.html %}


## 링크

-   **LIVE** : <a href="{{ site.baseurl }}/redirect/financiar/">{{ site.baseurl }}/redirect/financiar/</a>
-   **REPO** : <a href="<https://github.com/iwakura1ain/Financiar>"><https://github.com/iwakura1ain/Financiar></a>


## 인원과 역할

-   **안창언**: 팀장, 시스템/스키마 설계, 프론트엔드, 백엔드
-   한수현: 프론트엔드


# 프로젝트


## S&P500에 해당하는 주식 종목 검색, 조회

-   주식의 **정보와 로고** 를 크롤링하여 mariadb에 저장
-   **무한 스크롤** 을 도입하여 사용자에게 정보를 계속적으로 제공
-   종목 이름별, 분야별 **검색 가능**

![img](./financiar-search.png)


## 주가 데이터를 그래프 형태로 표출

-   주가 정보를 Yahoo Finance에서 크롤링 해 표출
-   그래프는 스크롤과 줌 가능, 이때 **스크롤시 데이터를 prefetch** 해서 로딩속도 감소
-   주가, 거래량, 가중평균, 당일변동 표출
-   다양한 차트 스타일 제공 (캔들, 바, 라인)

![img](./financiar-chart.png)


## Redis를 사용한 데이터 캐싱 사용

-   주가 데이터를 **redis에 캐싱** 하여 API 응답 시간을 낮춤
    ![img](./financiar-redis.png)
