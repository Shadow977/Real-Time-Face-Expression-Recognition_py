# Real-Time-Facial-Expression-Recognition
A real-time facial expression recognition system through webcam streaming and CNN.

## Abstract
This project aims to recognize facial expression with CNN implemented by Keras. I also implement a real-time module which can real-time capture user's face through webcam steaming called by opencv. OpenCV cropped the face it detects from the original frames and resize the cropped images to 48x48 grayscale image, then take them as inputs of deep leanring model. Moreover, this project also provides a function to combine users' spoken content and  facial expression detected by our system to generate corresponding sentences with appropriate emoticons.

## Dataset
[fer2013](https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data) is the dataset I chose, which is anounced in Kaggle competition in 2013.

## Environment
I provide my work environment for references.

### Hadware
CPU : i7-9750H 
GPU : nvidia GTX 1660ti 6G
RAM : 16G  

### Software
OS  : Windows 10 1909  
Keras 2.3.1 
opencv 4.2.0 
Tensorflow GPU 2.1.0

## Installation
I strongly recommend you to use [`Anaconda`](https://www.continuum.io/downloads), which is a package manager and provides python virtual environment.  
After you install Anaconda, you can create a virtual environment with python 3.4.
```
conda create -n env-name python=3.5.4
```
you can also check if your env. has been created by,
```
conda info --envs
```
You should activate your virtual environment in different way corresponding to your operating system.
For example, In Ubuntu, you can activate your virtual environment by,
```
source activate env-name
```
And,
```
source deactivate 
```
to exit the virtual environment.

The following instructions will lead you to install dependencies, and I suggest you to fllow the order.

#### Install OpenCV
Note that the version `Anaconda` provided may not be the latest one.
```
conda install opencv
```
If you fail to install opencv due to python version conflicts, try this command instead,
```
conda install -c menpo opencv4=4.2.0
```
the version 4.2.0 can be replaced with the lateset one, but in this project, I use `opencv 4.2.0`.

#### Install Tensorflow GPU

```
pip install tensorflow-gpu
```


#### Install Keras
Keras is a high-level wrapper of Theano and Tensorflow, it provides friendly APIs to manipulate several kinds of deep learning models.
```
pip install --upgrade keras
```
#### Install pandas and h5py
`pandas` can help you to preprocess data if you want train your own deep learning model.
```
conda install pandas
```
`h5py` is used to save weights of pre-trained models.
```
conda install h5py
```

## Usage
### Simple facial expression detection
After installing dependencies, you can move to `root` directory and simply type this command,
```
python main.py
```
and the system will start detecting user's emotions and print results to the console.  

### Switching Between Webcam and File from Computer
Just open the `Camera.py` file and in the line

```
self.video = cv2.VideoCapture(0)
```
Replace `0` with `File Directory`

```
self.video = cv2.VideoCapture("File name")
```

## Contact
Please give me a star if you like my project.
