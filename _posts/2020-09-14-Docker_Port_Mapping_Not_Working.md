---
layout: post #jekyll layout
title: "Docker Port Mapping Not Working" #title 
date:   2020-09-14 15:20:05 +0900                 
---

-   Docker port mapping not working

-   try building with no cache

    docker compose build --no-cache

-   try deleting docker image then rebuilding

    docker image ls
    docker image rm [image-name] -f

-   try pruning system then rebuilding

    docker system prune
    docker build [dockerfile-directory]

-   try running with run instead of docker compose up

    docker run -p "1000:1000" [image-name]

