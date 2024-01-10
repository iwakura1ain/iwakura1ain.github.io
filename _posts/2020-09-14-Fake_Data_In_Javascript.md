---
title: "Fake Data In Javascript"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   fake data in javascript

    use faker library

{% highlight bash %}
npm i faker
{% endhighlight %}

{% highlight javascript %}
import faker from "faker";

const bigList = [...Array(5000)].map(() => ({
    name: faker.name.findName(),
    email: faker.internet.email(),
    avatar: faker.internet.avatar()
}));
{% endhighlight %}
