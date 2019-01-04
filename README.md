# O'Reilly Apache MXNet Workshop Lab Materials

* **Workshop Name:** Applied Deep Learning for coders with Apache MXNet - Hands-on deep learning in Computer Vision and Natural Language Processing

* **Workshop link:** https://www.safaribooksonline.com/live-training/courses/applied-deep-learning-for-coders-with-apache-mxnet/0636920232841/

# Lab Exercises

1. [Lab 1 - Basics of NDArray (Tensors) - Fundamental Datastructure in Deep Learning](https://github.com/sandeep-krishnamurthy/oreilly-mxnet-workshop/tree/master/lab1-ndarray-basics)
2. [Lab 2 - Fashion MNIST - Train your first Neural Network in Gluon - Multi Layer Perceptron(MLP)](https://github.com/sandeep-krishnamurthy/oreilly-mxnet-workshop/tree/master/lab2-mlp-fashion-mnist)
3. [Lab 3 - Facial Emotion Recognition in Gluon - Intuition behind Convolutional Neural Networks(CNN)](https://github.com/sandeep-krishnamurthy/oreilly-mxnet-workshop/tree/master/lab3-cnn-facial-emotion-recognition)
4. [Lab 4 - Text to Emoji Prediction in Gluon - Intuition behind Recurrent Neural Networks(RNN)](https://github.com/sandeep-krishnamurthy/oreilly-mxnet-workshop/tree/master/lab4-rnn-text-to-emoji)

# Prerequisites / Installation

## (Option 1) On Ubuntu / Mac

### Install Anaconda and Setup Conda Environment

1. Install Anaconda - https://docs.continuum.io/anaconda/install/mac-os.html 
2. Set up Conda Environment for MXNet development

Execute the below commands for the first time, when you are setting up your machine:

```
# Download this repository with lab exercises and resources
$ git clone  https://github.com/sandeep-krishnamurthy/oreilly-mxnet-workshop
```

```
# Create a conda environment with name "mxnet_dev"
$ conda create -n mxnet_dev python=3 numpy jupyter

# Activate
$ source activate mxnet_dev

# Install MXNet

(mxnet_dev) $ pip install mxnet-mkl # for CPU machines
(mxnet_dev) $ pip install mxnet-cu92 # for GPU machines with CUDA 9.2

# Dependencies for CNN Lab exercise
(mxnet_dev) $ pip install Pillow # For image processing
(mxnet_dev) $ pip install graphviz # For MXNet network visualization
(mxnet_dev) $ pip install matplotlib # For plotting training graphs

# Dependencies for RNN Lab exercise
(mxnet_dev) $ pip install emoji
(mxnet_dev) $ pip install gluon-nlp
(mxnet_dev) $ pip install spacy -U --quiet
(mxnet_dev) $ python -m spacy download en

# Dependencies for model serving with MXNet Model Server
(mxnet_dev) $ pip install mxnet-model-server
(mxnet_dev) $ pip install scikit-image
(mxnet_dev) $ pip install opencv-python

# Deactivate the environment
(mxnet_dev) $ source deactivate
```

Execute, below command whenever you want to work with these Lab exercises:
**NOTE:** Make sure you have cloned (downloaded) this repository and you are in the downloaded directory (oreilly-mxnet-workshop)

```
# Activate the mxnet_dev conda environment we have prepared
$ source activate mxnet_dev

# Start Jupyter Notebook
(mxnet_dev) $ jupyter notebook

# When you are done. Deactivate the conda environment
(mxnet_dev) $ source deactivate
```

## (Option 2) Use cloud - AWS / Google Cloud

1. On AWS, you can use pre-configured Deep Learning AMIs, which comes with all frameworks and libraries pre-installed in Conda environments. You just need to launch an EC2 instance with Deep Learning AMI and then get started with coding! See [here for Instructions](https://aws.amazon.com/blogs/machine-learning/get-started-with-deep-learning-using-the-aws-deep-learning-ami/)

2. On Google Cloud, you can use pre-configured Deep Learning images. Similar to AWS Deep Learning AMI, all the deep learning frameworks and required library dependencies are pre-installed and you can just get started with coding! See [here for Instructions](https://cloud.google.com/deep-learning-vm/)

# Resources
1. Apache MXNet (Incubating) - http://mxnet.incubator.apache.org/
2. Learning Deep Learning with Gluon - https://gluon.mxnet.io/
3. (Highly Recommended) Dive into Deep Learning with Gluon - http://d2l.ai/

