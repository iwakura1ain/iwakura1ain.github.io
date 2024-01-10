---
title: "Python Order By Dict"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   python order by dict

{% highlight python %}
a = ['cd', 'ef', 'ab']
sorted(a)
print(a)	# ['ab', 'cd', 'ef']
{% endhighlight %}

{% highlight python %}
s = "adfe"

s1 = s.sort()			# wrong
s2 = sorted(s)			# ['a','d','e','f'] 
s3 = ''.join(sorted(s))		# "adef"
{% endhighlight %}
