---
title: "Docker Port Mapping Not Working"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   Docker port mapping not working

-   try building with no cache

{% highlight nil %}
docker compose build --no-cache
{% endhighlight %}

-   try deleting docker image then rebuilding

{% highlight bash %}
docker image ls
docker image rm [image-name] -f
{% endhighlight %}

-   try pruning system then rebuilding

{% highlight bash %}
docker system prune
docker build [dockerfile-directory]
{% endhighlight %}

-   try running with run instead of docker compose up

{% highlight bash %}
docker run -p "1000:1000" [image-name]
{% endhighlight %}
