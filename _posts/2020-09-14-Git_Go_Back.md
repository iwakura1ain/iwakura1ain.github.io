---
title: "Git Go Back"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   Git go back

-   Hard reset
    
        force reset 1 commit behind head
        will overwrite changes made
        always have commit log open and check after every reset

{% highlight bash %}
git reset --hard HEAD~
{% endhighlight %}

-   Soft reset
    
        force reset 1 commit behind head
        will not overwrite changes made

{% highlight bash %}
git reset --soft HEAD~
{% endhighlight %}

-   revert to commit id
    
        somehow doesnt revert merges?

{% highlight bash %}
git revert [commit-ID]
{% endhighlight %}
