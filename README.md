# Python install for Machine Learning Tensorflow Keras Windows 7 (in development)
Python install for Machine Learning (Tensorflow Keras) on Windows 7 (CPU)

###### What you will need :

- Windows 7
- Administrator rights

Hello! This post will aim at installing Python for Machine Learning with Keras on Windows 7.
At the end of this tutorial you will have installed the following:
- Python 3.5 (64-bit)
- Pip
- Tensorflow
- Keras
- Jupyter notebook

First, we need to install Python 3.5.2.
Download the Windows x86-64 executable installer at https://www.python.org/ftp/python/3.5.2/python-3.5.2-amd64.exe.

Install the program.

Open a Windows Terminal from Start >> All Programs >> Accessories >> Command Prompt and right click and choose "Run as administrator"

Check Python version by typing 
>python --version

It should read "Python 3.5.2".

Locate the python.exe file by typing python.exe in Start >> "Search programms and files" and right click on python and choose Properties. Copy the Location field.
In the command prompt, type cd\ and paste the path to python.exe

Now install and upgrade pip (a Python package manager) by entering the following command
>python.exe -m pip install --upgrade pip

Once it is done, install Tensorflow by typing
>pip install --upgrade tensorflow

Then install Keras with
>pip install --upgrade keras

Finally, install jupyter
>pip install jupyter

Start a notebook with the command
>jupyter notebook

The jupyter notebook should open in your web browser. If it doesn't, copy paste the link in terminal that looks like
>http://localhost:8888/?token=31314d79ccf87a3d79cc377808db8cda06d84196887d0e0f

You can navigate in your file system. I will go to /Documents and then click on "New" and choose "Python 3".
It will create an Untitled python file.

Once it is done, you're good to go!
You can start writing your python code!

You can try to run the following "hello world"
```
import tensorflow as tf
mnist = tf.keras.datasets.mnist

(x_train, y_train),(x_test, y_test) = mnist.load_data()
x_train, x_test = x_train / 255.0, x_test / 255.0

model = tf.keras.models.Sequential([
  tf.keras.layers.Flatten(),
  tf.keras.layers.Dense(512, activation=tf.nn.relu),
  tf.keras.layers.Dropout(0.2),
  tf.keras.layers.Dense(10, activation=tf.nn.softmax)
])
model.compile(optimizer='adam',
              loss='sparse_categorical_crossentropy',
              metrics=['accuracy'])

model.fit(x_train, y_train, epochs=5)
model.evaluate(x_test, y_test)
```

The result should be something like that (showing the training):

![alt text](https://github.com/pleboulanger/Python-install-for-Machine-Learning-Tensorflow-Keras-Windows-7/blob/master/MNIST.PNG)

###### Sources :

Python
https://www.python.org/downloads/release/python-352/

Pip
https://pypi.org/project/pip/

Tensorflow
https://www.tensorflow.org/install

For GPU:
https://medium.com/@kelfun5354/step-by-step-guide-to-install-tensorflow-cpu-gpu-for-windows-7-b472327984cd

Keras:
https://keras.io/#installation

Jupyter:
https://jupyter.readthedocs.io/en/latest/install.html
