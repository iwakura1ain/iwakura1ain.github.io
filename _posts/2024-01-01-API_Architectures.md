
# Table of Contents

1.  [API Architectures](#org88d1e87)
    1.  [SOAP](#orgb851be9)
    2.  [REST](#org8508c57)
    3.  [GraphQL](#orgfabdd9b)
    4.  [gRPC](#orgb5f628e)
    5.  [WebSocket](#orgce80f05)
    6.  [WebHook](#org5c58578)


<a id="org88d1e87"></a>

# API Architectures


<a id="orgb851be9"></a>

## SOAP

-   XML based enterprise architecture
-   secure/reliable -> used in financial sector
-   verbose and heavy


<a id="org8508c57"></a>

## REST

-   Resource based for web servers
-   synchronous/latency data is difficult


<a id="orgfabdd9b"></a>

## GraphQL

-   query language for reduced network load
-   query only what you want, no over/under fetching


<a id="orgb5f628e"></a>

## gRPC

-   High performance for microservices
-   low web browser support


<a id="orgce80f05"></a>

## WebSocket

-   Bi-directional low latency data exchange
-   open socket may be unnessesary overhead


<a id="org5c58578"></a>

## WebHook

-   asynchronous for event driven application
-   response receiving might fail -> must implement safety measures

