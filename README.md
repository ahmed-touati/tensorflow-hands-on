# tensorflow-hands-on

This repository is meant to share materials about deep learning and TensorFlow used during my two interventions at training program 
<a href="http://portail-formation.cnam.fr/ecole-siti/ingenierie-mathematique/statistique-bioinformatique/certificat-de-specialisation-analyste-de-donnees-massives-669531.kjsp?RH=204">Certificat de spécialisation Analyste de données massives</a>
in <a href="http://www.cnam.fr/">Conservatoire national des arts et métiers</a>.

# Deep learning Slides

If you would like to have a quick overview of deep learning basic architectures and its applications in computer vision and Natural language processing,
you could find the presentation in the following link: http://ahmed-touati.github.io/tensorflow-hands-on/

# Hands on and installation

This hands-on is meant to dive into the Google open-sourced machine learning library <a href="https://www.tensorflow.org/">TensorFlow</a>. 
Coding will be in Python 2.7 using <a href="http://ipython.org/notebook.html">IPython Notebook</a>.

This hands-on is inspired from the udacity course of deep learning: https://www.udacity.com/course/deep-learning--ud730.

I will explain here how to install TensorFlow on Mac or Linux.
For the windows users, you could follow the instructions described in <a href="http://www.netinstructions.com/how-to-install-and-run-tensorflow-on-a-windows-pc/">How to install and run TensorFlow on a Windows PC</a>. However, windows users should read this following tutorial especially the last section as the instructions are a bit similar for the three operating systems.

There are three types of install:
<ul>
	<li><strong>Pip</strong>: Install TensorFlow directly on your computer. You need to have Python 2.7 and pip installed</li>
	<li><strong>Virtualenv</strong>: Install TensorFlow in an isolated (virtual) Python environment.</li>
	<li><strong>Docker</strong>: Run TensorFlow in an isolated Docker container (virtual machine) on your computer.</li>
</ul>

If you would like to use the two first methods, You could follow instructions in <a href="https://www.tensorflow.org/versions/master/get_started/os_setup.html#download-and-setup"> download and setup TensorFlow</a>.

Here, I will explain the Docker method. I think it is the easiest method as it ensures that all dependencies required are available.
It could be confusing to use docker initially. Docker is very useful to package a piece of software with all its dependencies. Moreover, it allows us to have the same developpement environnement through the training session.
## Setup

1. Install docker. Follow the instructions in: 
	* https://docs.docker.com/mac/step_one/ for Mac
	* https://docs.docker.com/engine/installation/ for Linux and choose your Linux distribution
2. Mac users should open "Docker Quickstart Terminal"
3. Type: ```docker run -p 8888:8888 -it b.gcr.io/tensorflow/tensorflow /bin/bash```
	* ```docker run``` : to run a given image.
	* ```-i``` : stands for interactive.
	* ```b.gcr.io/tensorflow/tensorflow``` : one of TensorFlow images provided by Google. when run this command at the first time, we will get the following response: ```Unable to find image 'b.gcr.io/tensorflow/tensorflow:latest' locally latest: Pulling from tensorflow/tensorflow``` and the download of the image from Google Cloud Repository will start. It will take some minutes.
	* ```/bin/bash``` : is the process to launch
##Testing
Type "ipython". After getting the promt of ipython, type the following code lines.
![](images/testing_docker.png)
After you type the last line you should see a response "Hello, World!".
## IPython Notebook
In the TensorFlow image, we can find three ipython notebooks in the "notebooks" folders: 1_hello_tensorflow.ipynb, 2_getting_started.ipynb, 3_mnist_from_scratch.ipynb.

The IPython Notebook is an interactive computational environment, in which you can combine code execution, text, mathematics, plots.

Type ```ipython notebook``` to launch IPython Notebook web application. 
To get access to the Notebooks, go to the browser and

* type http://127.0.0.1:8888 on Linux.
* On mac, find the virtual machine's IP using:
	* ```docker-machine ip default``` 
	* Then go to: http://IP:8888 (likely http://192.168.99.100:8888)

We could see on the browser the three notebooks.
![](images/notebooks.png)
Click for example on the first one "1_hello_tensorflow.ipynb".
The notebook is split into cells: a cell can contain python code or text. You can execute a cell by clicking on it and pressing Shift-Enter. When you do so, the code in the cell will run, and the output of the cell will be displayed beneath the cell. You can also add more cells and write more codes.
![](images/notebooks_cells.png)
<strong color="red">I strongly recommand you to read those three notebooks and play with before the our training session.</strong>

