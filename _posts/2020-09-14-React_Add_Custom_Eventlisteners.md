---
title: "React Add Custom Eventlisteners"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   React add custom eventlisteners

-   add eventlistener using useEffect

{% highlight javascript %}
  useEffect(() => {
    window.addEventListener("scroll", callbackFunction);  // add eventListener
    return () =>
    window.removeEventListener("scroll", callbackFunction);  // return eventListener remover function
}, [])
{% endhighlight %}

-   callback function for scrolling

{% highlight javascript %}
  const listenToScroll = () => {
    let heightToHideFrom = 500;
    const winScroll = document.body.scrollTop ||
          document.documentElement.scrollTop;

    if (winScroll < heightToHideFrom) {
        // visibility &&      // to limit setting state only the first time
        setVisibility(false);
    } else {
        setVisibility(true);
    }
}  
{% endhighlight %}
