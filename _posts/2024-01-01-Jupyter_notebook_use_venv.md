
# Table of Contents

1.  [Jupyter notebook use venv](#orga00f919)


<a id="orga00f919"></a>

# Jupyter notebook use venv

<https://janakiev.com/blog/jupyter-virtual-envs/>

-   First, make sure your environment is activated.
-   Next, install ipykernel which provides the IPython kernel for Jupyter.

    pip install --user ipykernel

-   Next you can add your virtual environment to Jupyter by typing:

    python -m ipykernel install --user --name=myenv

    Installed kernelspec myenv in /home/user/.local/share/jupyter/kernels/myenv

-   In this folder you will find a kernel.json file which should look the following way if you did everything correctly:

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

-   After you deleted your virtual environment, you’ll want to remove it also from Jupyter. Let’s first see which kernels are available. You can list them with:

    jupyter kernelspec list

    Available kernels:
      myenv      /home/user/.local/share/jupyter/kernels/myenv
      python3    /usr/local/share/jupyter/kernels/python3

-   Now, to uninstall the kernel, you can type:

    jupyter kernelspec uninstall myenv

-   Optionally on Emacs ein, select which kernel to use on main screen.

