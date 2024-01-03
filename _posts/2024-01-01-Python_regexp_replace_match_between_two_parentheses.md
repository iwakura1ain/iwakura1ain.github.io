
# Table of Contents

1.  [Python regexp replace match between two parentheses](#org32fdedc)


<a id="org32fdedc"></a>

# Python regexp replace match between two parentheses

    import re
    # match everything between "[" and "]", note the escape characters 
    desc = re.sub("\[(.*?)\]", "", info_val["desc"])

