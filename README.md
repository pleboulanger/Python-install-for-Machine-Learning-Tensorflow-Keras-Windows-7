# Python-install-for-Machine-Learning-Tensorflow-Keras-Windows-7
Python install for Machine Learning (Tensorflow Keras) on Windows 7 

What you will need :

-Windows 7
-Administrator rights

Hello! This post will aim at installing Python for Machine Learning with Keras on Windows 7.
At the end of this tutorial you will have installed the following:
-Python 3.5 (64-bit)
-Pip
-Tensorflow
-Keras

First, we need to install Python 3.5.2.
Go to https://www.python.org/downloads/release/python-352/ and download the Windows x86-64 executable installer.

Install the program.

Open a Windows Terminal from Start >> All Programs >> Accessories >> Command Prompt and right click and choose "Run as administrator"

Check Python version by typing 
python --version

It should read "Python 3.5.2".

Locate the python.exe file by typing python.exe in Start >> "Search programms and files" and right click on python and choose Properties. Copy the Location field.
In the command prompt, type cd\ and paste the path to python.exe

Now install and upgrade pip (a Python package manager) by entering the following command
python.exe -m pip install --upgrade pip

Once it is done, install Tensorflow by typing
pip install --upgrade tensorflow

Then install Keras with
pip install --upgrade keras

Once it is done, you're good to go!
If you want an IDE in order to write your code, you can get PyCharm Community from https://www.jetbrains.com/pycharm/download/#section=windows
