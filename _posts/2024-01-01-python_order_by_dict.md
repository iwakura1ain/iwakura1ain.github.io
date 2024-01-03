
# Table of Contents

1.  [python order by dict](#org505b91d)


<a id="org505b91d"></a>

# python order by dict

    a = ['cd', 'ef', 'ab']
    sorted(a)
    print(a)	# ['ab', 'cd', 'ef']

    s = "adfe"
    
    s1 = s.sort()			# wrong
    s2 = sorted(s)			# ['a','d','e','f'] 
    s3 = ''.join(sorted(s))		# "adef"

