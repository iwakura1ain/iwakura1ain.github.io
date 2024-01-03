---
layout: post #jekyll layout
title: "Git Go Back" #title 
date:   2020-09-14 15:20:05 +0900                 
---

-   Git go back

-   Hard reset
    
        force reset 1 commit behind head
        will overwrite changes made
        always have commit log open and check after every reset

    git reset --hard HEAD~

-   Soft reset
    
        force reset 1 commit behind head
        will not overwrite changes made

    git reset --soft HEAD~

-   revert to commit id
    
        somehow doesnt revert merges?

    git revert [commit-ID]

