---
layout: post #jekyll layout
title: "Python Selenium Crawling Quickstart" #title 
date:   2020-09-14 15:20:05 +0900                 
---

-   Python Selenium Crawling Quickstart

-   create webdriver

    from selenium import webdriver
    driver = webdriver.Firefox()
    driver.implicitly_wait(5)

-   get page and element inside page

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

-   select inner element by XPATH

    xpath = ".//div[4]/div[1]/div[last()-1]"
    inner_element = element.find_elements(By.XPATH, xpath)
    inner_element.text

