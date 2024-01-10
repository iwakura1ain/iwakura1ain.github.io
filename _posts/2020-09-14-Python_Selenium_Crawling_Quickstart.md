---
title: "Python Selenium Crawling Quickstart"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   Python Selenium Crawling Quickstart

-   create webdriver

{% highlight python %}
from selenium import webdriver
driver = webdriver.Firefox()
driver.implicitly_wait(5)
{% endhighlight %}

-   get page and element inside page

{% highlight python %}
from selenium.webdriver.common.by import By

# ========= By module ==========
# ID = "id"
# NAME = "name"
# XPATH = "xpath"
# LINK_TEXT = "link text"
# PARTIAL_LINK_TEXT = "partial link text"
# TAG_NAME = "tag name"
# CLASS_NAME = "class name"
# CSS_SELECTOR = "css selector"
element = driver.find_element(by=By.ID, value="constituents")
{% endhighlight %}

-   select inner element by XPATH

{% highlight python %}
xpath = ".//div[4]/div[1]/div[last()-1]"
inner_element = element.find_elements(By.XPATH, xpath)
inner_element.text
{% endhighlight %}
