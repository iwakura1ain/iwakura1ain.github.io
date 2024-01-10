---
title: "Python Read And Write Json From File"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   python read and write json from file

{% highlight python %}
import json

  # JSON file
  f = open ('data.json', "r")

  # Reading from file
  data = json.loads(f.read())

  # Iterating through the json list
  for i in data['emp_details']:
      print(i)

  # Closing file
  f.close()

  # Serializing json
json_object = json.dumps(dictionary, indent=4)

# Writing to sample.json
with open("sample.json", "w") as outfile:
    outfile.write(json_object)
{% endhighlight %}
