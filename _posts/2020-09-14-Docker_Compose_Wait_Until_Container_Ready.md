---
title: "Docker Compose Wait Until Container Ready"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   docker compose wait until container ready

-   configure depends<sub>on</sub>

{% highlight yaml %}
depends_on:
  "service name"
{% endhighlight %}

-   configure depends<sub>on</sub> + healthcheck

{% highlight yaml %}
depends_on:
  "service name":
    condition: "service_started" | "service_healthy" | "service_completed_successfully"

...
service:
  healthcheck:
    test: curl --fail http://localhost:6379 || exit 1
    interval: 5s
    retries: 5
    start_period: 5s
    timeout: 10s
{% endhighlight %}
