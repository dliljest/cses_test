# Getting Started: Virtual Environment
It is a best practice to create a virtual environment when starting a new project, as a virtual environment essentially creates an isolated working copy of Python for a particular project. 
I.e., each environment can have its own dependencies or even its own Python versions.
Creating a Python virtual environment is useful if you need different versions of Python or packages for different projects.
Lastly, a virtual environment keeps things tidy, makes sure your main Python installation stays healthy and supports reproducible and open science.

## Creating your Python-GEE Virtual Environment
Since we will be using Jupyter Notebooks for this exercise, we will use the Anaconda command prompt to create our virtual environment. 
In the command line type: 

    conda create -n GEE_env python=3.9.12

For this example, we will be using Python version 3.9.12, specify this version when setting up your new virtual environment.
After Anaconda finishes setting up your GEE_env, activate it using the activate function.

    conda activate GEE_env

You should now be working in your new GEE_env within the command prompt. 
However, we will want to work in this environment within our Jupyter Notebook and need to create a kernel to connect them.
We begin by installing the **ipykernel** python package:

    pip install --user ipykernel

With the package installed, we can connect the GEE_env to our Python Notebook

    python -m ipykernel install --user --name=GEE_env

Open up the [ROSET-AWS.ipynb](./ROSET-AWS/ROSET_AWS.ipynb.ipynb) file, click the kernel tab on the top toolbar, and select the GEE_env. 
The GEE_env should show up on the top right of the Jupyter Notebook.

![GEE_Notebook_GEE_env](./Images/GEE_Jupyter_Kernel2.JPG)



## Loading other Python dependencies
We will now be installing the packages needed to use ROSET-AWS, as well as other tools to accomplish data science tasks.
Enter the following code block in your Anaconda Command Prompt to get the required dependencies with the appropriate versions, note, you must be in the correct working directory:

    pip install -r requirements.txt