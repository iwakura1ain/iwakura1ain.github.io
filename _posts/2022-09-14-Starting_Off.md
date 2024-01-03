---
layout: post #jekyll layout
title: "Starting Off" #title 
date:   2022-09-14 15:20:05 +0900
categories: #specify post category (space seperated string)
tags: #specify post tags (space seperated string)
#variable: val -> use as {{page.variable}}
---

# About this Blog

This blog is primarily running **Jekyll** integrated with **Emacs** and **org-mode**.
I've also added some helper functions that lets me publish org files into markdown, which is then processed by jekyll.

The following is a modified elisp function that publishes org files into markdown for processing by jekyll.

    ;;org blogging
    (defun org-md-publish-to-md (plist filename org-export-publishing-directory)
      "Publish an org file to Markdown.
    
    FILENAME is the filename of the Org file to be published.  PLIST
    is the property list for the given project.  PUB-DIR is the
    publishing directory.
    
    Return output file name."
      (org-publish-org-to 'md filename ".markdown" plist org-export-publishing-directory))
    
    ;;org blogging https://orgmode.org/worg/org-tutorials/org-jekyll.html
    (setq org-publish-project-alist '(
            ("org-blog-export"
               :base-directory "/home/dks/Development/Blog/org"
               :base-extension "org"
             ;; Path to your Jekyll project.
             :publishing-directory "/home/dks/Development/Blog/_posts"
             :publishing-function org-md-publish-to-md
             :headline-levels 4
             ;;:md-extension "markdown"
             ;;:body-only t ;; Only export section between <body> </body>
             )
    
    
    
            ("org-blog-static-export"
             :base-directory "/home/dks/Development/Blog/org"
             :base-extension "css\\|js\\|png\\|jpg\\|gif\\|pdf\\|mp3\\|ogg\\|swf\\|php"
             :publishing-directory "/home/dks/Development/Blog/assets"
             :recursive t
             :publishing-function org-publish-attachment)
    
            ("blog-export" :components ("org-blog-export" "org-blog-static-export"))
            ))

