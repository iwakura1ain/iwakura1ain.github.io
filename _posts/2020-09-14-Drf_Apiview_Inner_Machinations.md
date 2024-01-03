---
layout: post #jekyll layout
title: "Drf Apiview Inner Machinations" #title 
date:   2020-09-14 15:20:05 +0900                 
---

-   DRF APIView inner machinations

1.  user requests HTTP method endpoint
2.  sent to HTTP method handler inside implemented generic APIView (eg. get(), post(), &#x2026;)
3.  handler calls apropriate method from mixed-in mixin class (eg. list(), destroy(), update(), &#x2026;)
4.  inside mixin class method  get<sub>queryset</sub>() -> filter<sub>queryset</sub>() to get current model
5.  paginates response with paginate<sub>queryset</sub>()
6.  gets serializer with get<sub>serializer</sub>() -> serializes model
7.  serialized data -> returns Response()

