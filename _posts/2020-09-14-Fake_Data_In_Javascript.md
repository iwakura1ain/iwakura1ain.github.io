---
layout: post #jekyll layout
title: "Fake Data In Javascript" #title 
date:   2020-09-14 15:20:05 +0900                 
---

-   fake data in javascript

    use faker library

    npm i faker

    import faker from "faker";
    
    const bigList = [...Array(5000)].map(() => ({
        name: faker.name.findName(),
        email: faker.internet.email(),
        avatar: faker.internet.avatar()
    }));

