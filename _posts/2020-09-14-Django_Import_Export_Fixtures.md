---
title: "Django Import Export Fixtures"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   Django import export fixtures

{% highlight bash %}
./manage.py loaddata [fixture-name]
./manage.py dumpdata app.model_name --indent 4 > [fixture-name].json
{% endhighlight %}
