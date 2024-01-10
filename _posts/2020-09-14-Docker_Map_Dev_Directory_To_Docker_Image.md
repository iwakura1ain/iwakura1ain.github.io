---
title: "Docker Map Dev Directory To Docker Image"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   Docker map dev directory to docker image

    PROS: container updates when you update local code

{% highlight yaml %}
service-name:
  ...
  volumes:
    - ./development/directory:/deployment/directory
{% endhighlight %}
