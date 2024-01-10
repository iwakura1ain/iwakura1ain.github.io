---
title: "Vite Cors Error On Development Server"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   vite CORS error on development server

<https://vitejs.dev/config/server-options.html>

    change request uri to local uri -> rewrite to external uri inside vite configs
    then request to local uri

{% highlight javascript %}
// in vite.config.ts
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react-swc';

// https://vitejs.dev/config/
export default defineConfig({
    plugins: [
        react()
    ],
    server: {
        proxy: {
            // "/api/something" --rewrite--> "http://api.github.com/something"
            '/api': {
                target: 'http://api.github.com',
                changeOrigin: true,
                rewrite: (path) => path.replace(/^\/api/, ''),
                secure: false,
                ws: true
            }
        }
    }
});
{% endhighlight %}
