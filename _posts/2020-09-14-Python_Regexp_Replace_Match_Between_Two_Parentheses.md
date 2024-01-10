---
title: "Python Regexp Replace Match Between Two Parentheses"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   Python regexp replace match between two parentheses

{% highlight python %}
import re
# match everything between "[" and "]", note the escape characters 
desc = re.sub("\[(.*?)\]", "", info_val["desc"])
{% endhighlight %}
