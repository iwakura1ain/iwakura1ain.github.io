---
layout: post #jekyll layout
title: "Docker Map Dev Directory To Docker Image" #title 
date:   2020-09-14 15:20:05 +0900                 
---

-   Docker map dev directory to docker image

    PROS: container updates when you update local code

    service-name:
      ...
      volumes:
        - ./development/directory:/deployment/directory

