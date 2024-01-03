---
layout: post #jekyll layout
title: "Api Architectures" #title 
date:   2020-09-14 15:20:05 +0900                 
---

-   API Architectures


# SOAP

-   XML based enterprise architecture
-   secure/reliable -> used in financial sector
-   verbose and heavy


# REST

-   Resource based for web servers
-   synchronous/latency data is difficult


# GraphQL

-   query language for reduced network load
-   query only what you want, no over/under fetching


# gRPC

-   High performance for microservices
-   low web browser support


# WebSocket

-   Bi-directional low latency data exchange
-   open socket may be unnessesary overhead


# WebHook

-   asynchronous for event driven application
-   response receiving might fail -> must implement safety measures

