---
layout: project
title: Fuzzit Input Scanner
desc: 웹서비스 인젝션 탐지 스캐너
categories: python multithreading injection
repo: https://github.com/iwakura1ain/Fuzzit-Web-Scanner
---
# Fuzzit-Web-Scanner
>Simple web input/cookie/url scanner written in python.
>Uses a json rule file to match injection cases against web app output.

Supported: Get, Post value injections, Cookie injection, and Page Discovery.


# Usage

``` shell
    Fuzzit.py [RHOST] [WORDLIST] [RULE_FILE]

    RHOST Format: www.url.com/script.php?injection_point=*
        - Mark injection points with a '*'.
        - Input values for non-injection points.
        - For status scans, mark a single '*' where WORDLIST will be appended.

    -t, --type [get/post/cookie/status]
        - get: Send a get request with values from WORDLIST.
        - post: Send a post request with values from WORDLIST.
        - cookie: Send a get request with cookie values from WORDLIST.
        - status: Check if a url from WORDLIST exists.

    -c, --cookie [COOKIE]
        - Specify cookie.
    --cookie-file [FILE]
        - Specify cookie from file.

    -o, --output [FILE]
        - Output to FILE

    -v, -vv
        - v: Show NEGATIVE requests and headers.
        - vv: Show response page.
```
