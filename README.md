# Creating an AI app that detects diseases in plants using Facebook’s deep learning platform: PyTorch
<img src="https://cdn-images-1.medium.com/max/800/1*IbJF_6mRTMsG9gL0j8uz5Q.jpeg">

According to the Food and Agriculture organization of the United Nations (UN), transboundary plant pests and diseases affect food crops, causing significant losses to farmers and threatening food security.

Plant diseases contribute 10–16% losses in the global harvest of crops each year costing an estimated US$220 billion. According to a report of the Food and Agriculture Organization (FAO), our world population is anticipated to hit 9.1 billion in 2050. Therefore, agricultural production needs to be increased up to 70% to fulfill the food requirements of a steadily growing population. On the other hand, abundant use of chemicals such as bactericides, fungicides, and nematicides to control plant diseases has been causing adverse effects in the agro-ecosystem. Currently, there is a need for effective early disease detection techniques to control plant diseases for food security and sustainability of agro-ecosystem.

The spread of transboundary plant pests and diseases has increased dramatically in recent years. Globalization, trade and climate change, as well as reduced resilience in production systems due to decades of agricultural intensification, have all played a part.

Transboundary plant pests and diseases can easily spread to several countries and reach epidemic proportions. Outbreaks and upsurges can cause huge losses to crops and pastures, threatening the livelihoods of vulnerable farmers and the food and nutrition security of millions at a time.

If you are into data science or machine learning, you’ve probably heard about these platforms crowdsourcing data challenges. The first that comes to my mind is Kaggle. Kaggle is this crowd-sourced platform that attracts, nurtures, trains and challenges data scientists from all around the world to solve data science, machine learning, and predictive analytics problems. This platform enables data scientists and other developers to engage in running machine learning contests, write and share code, and to host datasets.

Looking for project ideas and datasets, found out another platform similar to Kaggle, but as a non-profit, I’m talking about crowdAI. crowdAI also hosts open data science challenges and helps universities, government agencies, NGOs, or businesses to run and manage their data challenges. The crowdAI platform is an open source infrastructure that can immediately reach thousands of data scientists around the world to work on interesting data problems.

I wanted to mention crowdAI, because it was there where I found the “PlantVillage Disease Classification Challenge”. The goal of this competition was to develop algorithms than can accurately diagnose a disease based on an image.

This challenge has already ended but I wanted to approach the same goal, using a different Deep Learning framework: PyTorch. So, I developed an AI application using a deep learning model and the transfer learning technique.

Computer Vision is a field within deep learning that is growing up more everyday . There are many areas Computer Vision can help to. 

In this notebook I will implement a deep learning model that can identify plant diseases, using Pytorch framework,  a Convolutional Neural Network (CNN) architecture. The goal is to detect different plant diseases by looking a picture.

I'll train this image classifier to recognize the different plant diseases given an image.This can be implemented in a phone app that tells you the type of disease your camera is looking at. I will use the "Plant Village" dataset.

<B>The Plant Village Dataset</B>

The Plant Village dataset contains 38 different plant disease classes and one background class from Stanford's open dataset of background images.

The classes are:

- Apple___Apple_scab
- Apple___Black_rot
- Apple___Cedar_apple_rust
- Apple___healthy
- Blueberry___healthy
- Cherry_(including_sour)___Powdery_mildew
- Cherry_(including_sour)___healthy
- Corn_(maize)___Cercospora_leaf_spot Gray_leaf_spot
- Corn_(maize)___Common_rust_
- Corn_(maize)___Northern_Leaf_Blight
- Corn_(maize)___healthy
- Grape___Black_rot
- Grape___Esca_(Black_Measles)
- Grape___Leaf_blight_(Isariopsis_Leaf_Spot)
- Grape___healthy
- Orange___Haunglongbing_(Citrus_greening)
- Peach___Bacterial_spot
- Peach___healthy
- Pepper,_bell___Bacterial_spot
- Pepper,_bell___healthy
- Potato___Early_blight
- Potato___Late_blight
- Potato___health
- Raspberry___healthy
- Soybean___healthy
- Squash___Powdery_mildew
- Strawberry___Leaf_scorch
- Strawberry___healthy
- Tomato___Bacterial_spot
- Tomato___Early_blight
- Tomato___Late_blight
- Tomato___Leaf_Mold
- Tomato___Septoria_leaf_spot
- Tomato___Spider_mites Two-spotted_spider_mite
- Tomato___Target_Spot
- Tomato___Tomato_Yellow_Leaf_Curl_Virus
- Tomato___Tomato_mosaic_virus
- Tomato___healthy

<B>INSTRUCTIONS</B>

The project is broken down into multiple steps:

* Load and preprocess the image dataset
* Train the image classifier on your dataset
* Use the trained classifier to predict image content


Everything you need to recreate this project is on the jupyter notebook. Everything was coded in Google Colab, because of its GPU. I uploaded the dataset to Google Drive, so you can download it directly. For more details, the notebook includes the instructions to follow.

You can find the requirements in Requirements.txt, but everything is in the notebook, so you can install all by using pip install. I recommend using Google Colab.
 
This project is updated to be compatible with PyTorch 0.4.0



Paper: "Using Deep Learning for Image-Based Plant Disease Detection" by Sharada Prasanna Mohanty, David Hughes and Marcel Salathé. Read here: https://arxiv.org/ftp/arxiv/papers/1604/1604.03169.pdf


 
STEPS IN BRIEF


Deploying models to Android with TensorFlow Mobile involves three steps:
Convert your trained model to TensorFlow

1. Add TensorFlow Mobile as a dependency in your Android app
2. Write Java code to perform inference in your app with the TensorFlow model.
3. n this post, I’ll take you through the entire process and conclude with a working Android app infused with Image Recognition.

Converting PyTorch Models to Keras
This section is only for PyTorch developers. If you’re using Keras, you can skip ahead to the section Converting Keras Models to TensorFlow.
The first thing we need to do is transfer the parameters of our PyTorch model into its equivalent in Keras. To simplify this process, I’ve created a script to automate this conversion. In this tutorial, we’ll be using SqueezeNet, a mobile architecture that’s extremely small with a reasonable level of accuracy. Download the pre-trained model here (just 5mb!).
Before converting the weights, we need to define the SqueezeNet model in both PyTorch and Keras.
Define SqueezeNet in both frameworks and transfer the weights from PyTorch to Keras, as below.

Converting Keras to TensorFlow Models
At this point, you have a Keras model either converted from PyTorch or obtained directly from training with Keras. You can download the pre-trained Keras SqueezeNet model here. The next step is to take our entire model structure and weights and convert it into a production-ready TensorFlow model.
Create a new file ConvertToTensorflow.py and add the code below.



Adding TensorFlow Mobile to Your Project
TensorFlow has two mobile libraries, TensorFlow Mobile and TensorFlow Lite. The Lite version is designed to be extremely small in size, with the entire dependencies occupying just around 1Mb. Its models are also better optimized.
Lastly, on Android 8 and above, it’s accelerated with Android’s Neural Network API. However, unlike TensorFlow Mobile” it’s not production-ready, as a few layers might not work as well as intended yet. Furthermore, support for compiling the library and converting models to its native format is not yet supported on Windows. Hence, in this tutorial, I’ll stick to TensorFlow Mobile.
Using Android Studio, create a new Android project if you don’t have an existing one. Add TensorFlow Mobile as a dependency in your build.gradle file.
implementation ‘org.tensorflow:tensorflow-android:+’
Android studio will prompt you to synchronize gradle. Click Sync Now and wait until it’s done.
At this point, your setup is complete.


Adding TensorFlow Mobile to Your Project
TensorFlow has two mobile libraries, TensorFlow Mobile and TensorFlow Lite. The Lite version is designed to be extremely small in size, with the entire dependencies occupying just around 1Mb. Its models are also better optimized.
Lastly, on Android 8 and above, it’s accelerated with Android’s Neural Network API. However, unlike TensorFlow Mobile” it’s not production-ready, as a few layers might not work as well as intended yet. Furthermore, support for compiling the library and converting models to its native format is not yet supported on Windows. Hence, in this tutorial, I’ll stick to TensorFlow Mobile.
Using Android Studio, create a new Android project if you don’t have an existing one. Add TensorFlow Mobile as a dependency in your build.gradle file.
implementation ‘org.tensorflow:tensorflow-android:+’
Android studio will prompt you to synchronize gradle. Click Sync Now and wait until it’s done.
At this point, your setup is complete.


Create an ImageView and a TextView in your main activity. This’ll be used to display the image and the prediction.
In your main activity, you need to load the TensorFlow inference library and also initialize some class variables. Add the following before your onCreate method: