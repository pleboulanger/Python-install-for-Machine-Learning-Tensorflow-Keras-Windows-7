# Python install for Machine Learning Tensorflow Keras Windows 7
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

First, we need to install Python 3.5.2.
Go to https://www.python.org/downloads/release/python-352/ and download the Windows x86-64 executable installer.

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

Once it is done, you're good to go!
If you want an IDE in order to write your code, you can get PyCharm Community from https://www.jetbrains.com/pycharm/download/#section=windows


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
###### Sources :
https://www.tensorflow.org/install

For GPU:
https://medium.com/@kelfun5354/step-by-step-guide-to-install-tensorflow-cpu-gpu-for-windows-7-b472327984cd
