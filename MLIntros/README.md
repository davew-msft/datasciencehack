## Getting Started with Machine Learning for Computer Vision
This library contains some simple examples of basic Machine Learning concepts and techniques - focusing on computer vision. 

This only covers *possible solutions*, YMMV.  

You do NOT need to run these in your DSVM.  These can be run anytime/anywhere using notebooks.azure.com, or jupyterhub running in a container.  

The library includes the following notebooks:
- **01 - Python and Numpy.ipynb**: A basic introduction to the essential Python libraries and techniques you'll need, as well as some information to help you get started running code in notebooks.
- **02 - Image Processing Basics.ipynb**: Before you start to look at using machine learning for image classification, it's useful to know a little about how images are represented as data structures, and how to work with them. This notebooks covers some common image processing techniques.
- **03 - Introduction to Machine Learning.ipynb**: An introduction to *classification*, one of the key *supervised learning* problems that machine learning is used to solve. This notebook covers the basics of binary and multiclass classification.
- **04*x* - Deep Neural Networks (*framework*).ipynb**: An introduction to *deep learning*, a cutting-edge approah to machine learning based on modeling the way the human brain works. There are two variants of this notebook, each describing how to use a different commonly used deep learning framework (*PyTorch* or *Keras*).
- **05*x* - Image Classification with a CNN (*framework*).ipynb**: This notebook builds on deep neural network techniques to create a *convolutional neural network* (CNN) for image classification.
- **06*x* - Transfer Learning (*framework*).ipynb**: *Transfer learning* is an increasingly common approach in which you use a pre-trained model to extract image features, and add a custom linear layer to map those features to your own set of classes. There are PyTorch and Keras variants of this notebook.
- **07*x* - Deploying a Model with Azure ML (*framework*).ipynb**: *Azure Machine Learning* is a cloud service that you can use to train, validate, deploy, and manage machine learning models. In this notebook, you'll deploy a machine learning model as container-based web service.
- **08 - Classification with the Custom Vision Service.ipynb**: Instead of building your own image classification model, it's worth investigating the *Custom Vision* cognitive service; which provides a service for training and publishing an image classifier.
- **09 - Object Detection with the Custom Vision Service.ipynb**: The previous notebooks focused on *image classification* (in other words, categorizing images based on their contents). The next step in computer vision is *object detection*, in which you identify specific objects within images. This notebook introduces the concept and uses the *Custom Vision* cognitive service to build a simple example.

***Note**: The notebooks may be listed in multiple pages. Use the **<** and **>** links or page numbers under the file list to navigate through the pages!*