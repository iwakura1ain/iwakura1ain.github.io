---
title: ""Starting Off" #title"
date: 2022-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---


# Table of Contents

1.  [About this Blog](#org986368e)


<a id="org986368e"></a>

# About this Blog

This blog is primarily running **Jekyll** integrated with **Emacs** and **org-mode**.
I've also added some helper functions that lets me publish org files into markdown, which is then processed by jekyll.

-   Define exporter function *org-md-publish-to-md*
    
        export org -> markdown

{% highlight lisp %}
;; https://lists.gnu.org/archive/html/emacs-orgmode/2013-10/msg00543.html
(defun org-md-publish-to-md (plist filename org-export-publishing-directory)
  "Publish an org file to Markdown.

FILENAME is the filename of the Org file to be published.  PLIST
is the property list for the given project.  PUB-DIR is the
publishing directory.

Return output file name."
  (org-publish-org-to 'md filename ".markdown" plist org-export-publishing-directory))

{% endhighlight %}

-   Define UI list for publishing
    
        org file export + static file export = /blog-export/

{% highlight lisp %}
;;org blogging based off https://orgmode.org/worg/org-tutorials/org-jekyll.html
(setq org-publish-project-alist
      '(
        ;; org file publishing
        ("org-blog-export"
         ;; Path to your original org files.
         :base-directory "/home/dks/Development/Blog/org"
         :base-extension "org"

         ;; Path to your exported org files.
         :publishing-directory "/home/dks/Development/Blog/_posts"
         ;; Use previously defined exporter function
         :publishing-function org-md-publish-to-md
         :headline-levels 4
         ;;:md-extension "markdown"
         ;;:body-only t ;; Only export section between <body> </body>
         )

        ;; static content publishing
        ("org-blog-static-export"
         :base-directory "/home/dks/Development/Blog/org"
         :base-extension "css\\|js\\|png\\|jpg\\|gif\\|pdf\\|mp3\\|ogg\\|swf\\|php"
         :publishing-directory "/home/dks/Development/Blog/assets"
         :recursive t
         :publishing-function org-publish-attachment)

        ;; do both org and static publishing
        ("blog-export" :components ("org-blog-export" "org-blog-static-export"))
        ))
{% endhighlight %}
