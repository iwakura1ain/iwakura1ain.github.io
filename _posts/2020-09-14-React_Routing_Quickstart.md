---
title: "React Routing Quickstart"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   React Routing Quickstart

    using react-router-dom

-   start inside App.jsx

{% highlight javascript %}
import { BrowserRouter, Routes, Route } from "react-router-dom";

// App.jsx
return (<>
        <BrowserRouter>
          <Routes>
            <Route path="/" element={<Layout />}> // base layout for every page
              <Route index element={<Component />} /> // index page component
              <Route path="backtest" element={<Component />} /> // different page component
            </Route>
          </Routes>
        </BrowserRouter>
        </>)
{% endhighlight %}

-   base layout

{% highlight javascript %}
// Layout.jsx
export const Layout = () => {
        return (
            <>
              <NavBar/>
              <Outlet/>  // content for layout
              <Footer/>
            </>
        )
    };

{% endhighlight %}
