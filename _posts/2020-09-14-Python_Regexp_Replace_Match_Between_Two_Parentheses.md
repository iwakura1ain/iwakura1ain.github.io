---
layout: post #jekyll layout
title: "Python Regexp Replace Match Between Two Parentheses" #title 
date:   2020-09-14 15:20:05 +0900                 
---

-   Python regexp replace match between two parentheses

    import re
    # match everything between "[" and "]", note the escape characters 
    desc = re.sub("\[(.*?)\]", "", info_val["desc"])

