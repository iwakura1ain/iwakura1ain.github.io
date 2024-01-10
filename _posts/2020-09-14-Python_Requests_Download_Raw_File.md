---
title: "Python Requests Download Raw File"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   Python requests download raw file

{% highlight python %}
import requests
import shutil

r = requests.get(settings.STATICMAP_URL.format(**data), stream=True)
if r.status_code == 200:
    with open(path, 'wb') as f:
        r.raw.decode_content = True
        shutil.copyfileobj(r.raw, f)   
{% endhighlight %}
