---
title: Financiar
layout: project
desc: 백테스팅을 위한 주식 시각화/가상투자 서비스 
categories: html css js react django drf selenium redis docker docker-compose
repo: https://github.com/iwakura1ain/Financiar
---


# 개요

**현재 주식 데이터 조회와 과거 데이터를 기반으로 모의투자를 하는 웹서비스**

<span id="target"></span>


## 인원과 역할

-   **안창언**: 팀장, 시스템/스키마 설계, 프론트엔드, 백엔드
-   한수현: 프론트엔드


# 프로젝트


## S&P500에 해당하는 주식 종목 검색, 조회

-   Yahoo Finance를 크롤링한 데이터를 기반
-   종목 이름별, 분야별 검색 가능

![img](./financiar-search.png)


## 주가 데이터를 반응형 그래프 형태로 표출

-   스크롤, 줌, prefetch 기능

![img](./financiar-chart.png)


## Redis를 사용한 데이터 캐싱 사용

-   크롤링한 데이터를 redis에 캐싱
    ![img](./financiar-redis.png)


# 제한사항