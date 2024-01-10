---
title: "Jupyter Notebook Use Venv"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   Jupyter notebook use venv

<https://janakiev.com/blog/jupyter-virtual-envs/>

-   First, make sure your environment is activated.
-   Next, install ipykernel which provides the IPython kernel for Jupyter.

{% highlight nil %}
pip install --user ipykernel
{% endhighlight %}

-   Next you can add your virtual environment to Jupyter by typing:

{% highlight nil %}
python -m ipykernel install --user --name=myenv
{% endhighlight %}

    Installed kernelspec myenv in /home/user/.local/share/jupyter/kernels/myenv

-   In this folder you will find a kernel.json file which should look the following way if you did everything correctly:

{% highlight json %}
{
    "argv": [
        "/home/user/anaconda3/envs/myenv/bin/python",
        "-m",
        "ipykernel_launcher",
        "-f",
        "{connection_file}"
    ],
    "display_name": "myenv",
    "language": "python"
}
{% endhighlight %}

-   After you deleted your virtual environment, you’ll want to remove it also from Jupyter. Let’s first see which kernels are available. You can list them with:

{% highlight nil %}
jupyter kernelspec list
{% endhighlight %}

    Available kernels:
      myenv      /home/user/.local/share/jupyter/kernels/myenv
      python3    /usr/local/share/jupyter/kernels/python3

-   Now, to uninstall the kernel, you can type:

{% highlight nil %}
jupyter kernelspec uninstall myenv
{% endhighlight %}

-   Optionally on Emacs ein, select which kernel to use on main screen.
