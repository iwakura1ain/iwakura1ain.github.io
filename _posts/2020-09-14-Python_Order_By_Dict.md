---
layout: post #jekyll layout
title: "Python Order By Dict" #title 
date:   2020-09-14 15:20:05 +0900                 
---

-   python order by dict

    a = ['cd', 'ef', 'ab']
    sorted(a)
    print(a)	# ['ab', 'cd', 'ef']

    s = "adfe"
    
    s1 = s.sort()			# wrong
    s2 = sorted(s)			# ['a','d','e','f'] 
    s3 = ''.join(sorted(s))		# "adef"

