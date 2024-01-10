---
title: "Python Selenium Wait After Submit"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   Python selenium wait after submit

    check until url changes

{% highlight python %}
# save current page url
  current_url = driver.current_url

  # initiate page transition, e.g.:
  search_form.clear()
  search_form.send_keys(name)
  search_form.submit()

  # wait for URL to change with 15 seconds timeout
  WebDriverWait(driver, 15).until(EC.url_changes(current_url))

{% endhighlight %}
