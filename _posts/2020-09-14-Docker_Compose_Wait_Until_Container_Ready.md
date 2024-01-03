---
layout: post #jekyll layout
title: "Docker Compose Wait Until Container Ready" #title 
date:   2020-09-14 15:20:05 +0900                 
---

-   docker compose wait until container ready

-   configure depends<sub>on</sub>

    depends_on:
      "service name"

-   configure depends<sub>on</sub> + healthcheck

    depends_on:
      "service name":
        condition: "service_started" | "service_healthy" | "service_completed_successfully"
    
    ...
    service:
      healthcheck:
        test: curl --fail http://localhost:6379 || exit 1
        interval: 5s
        retries: 5
        start_period: 5s
        timeout: 10s

