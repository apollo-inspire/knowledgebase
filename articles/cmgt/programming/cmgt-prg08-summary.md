# Programmeren 8: Machine Learning
*Knowledgebase: https://luukftf.github.io/knowledgebase*  
*(code: https://github.com/LuukFTF/knowledgebase)*  
*By: Lucas van der Vegt*
*2022-02-15*
<!-- Editted by: NAME, NAME, NAME -->


## Leerdoelen

## Deadlines
Opdracht 1: Week 3
Opdracht 2: Week 5
Eindopdracht Ontwerp: Week 7
Eindopdracht Uitwerking: Week 9

## Index

## Resources

https://github.com/HR-CMGT/Machine-Learning-Readinglist

https://github.com/tensorflow/models/tree/master/research/slim

## Les 1

Tensorflow JS

voorbeelden:
- Tesla
- GPT3
- Google Search
- Youtube Recommendation

Resources
Kaggle.com

Teachable Machine

Waarom is ML nu populair
- Rekenkracht
- Data
- Mindset


Disciplines:
- Leren van data
- beeld herkenning

- beeld generen
- spraak begrijpen
- tekst genereren
- tekst begrijpen

**Artificial Intelligence**  
Dumb AI

**Machine Learning**    
Supervised Learning

**Deep Learning**  
Unsupervised Learning



Leren is patronen herkennen in data

Wat heb ik voor data?

Wat wil / kan ik leren van deze data

Welk algoritme of model past hierbij

Data > Algoritme > Model


**Data**  
alles is data, maak er een reeks van getallen voor


**Algoritme**  
De formule of library waarmee je een model maakt

**Model**  
Gegenereerd door algoritme dmv data


**Classification**  
verschillende keuzes

**Regression**  
een waarde 

**White Box & Black Box**  
Is het achteraf te begrijpen
(Ethiek)


We gaan aan de slag met:

Decision Tree KNN

Neural Network

Linear Regression


**Pretrained Model**  
Al getrained model

- YOLO
- FaceAPI
- PoseNet
- DoodleNet
- ImageClassify


Libraries:
- TensorFlow
- ML5

Ethiek
- Privacy
- White vs Black box


Techstack:
- TensorflowJS (alleen local vanwege privacy)
- Frontend React
- Backend NodeJS

## Les 2

### ML5 Introduction

**Datasets**
Kaggle

**Training Algoritme**
Neural Network
Linear Regression
Decision Tree
K-Means

**Model**
Maken door trainen
Pre-trained

**Examples**:
[Google Quickdraw](https://quickdraw.withgoogle.com/)
[Autodraw](https://www.autodraw.com/)
[Drawthis (danmacnish)](https://danmacnish.com/drawthis/)


**Pixel Data**
1 Color:
Grijswaardes per pixel (12x16 px = 192 waardes)

RGB:
Rood Groen & Blauw per pixel (12x16 px = 576 waardes)

**Convolutional neural networks** *< Een Convolutional Neural Network reduceert een afbeelding tot een heel klein stukje data, waar toch nog alle informatie in zit om te weten of een afbeelding een kat of een hond >*

https://www.youtube.com/watch?t=414&v=qPKsVAI_W6M&feature=youtu.be
https://www.youtube.com/watch?v=f0t-OCG79-U

Cat or Dog? (features data)
- hair color
- body length
- height
- weight
- ear length
- claws

**Features** *< De informatie die we gevonden hebben noemen we "features". Door op te slaan welke combinaties van features bij een "auto" horen kunnen we auto's herkennen >* 


### Pre-trained models: image classifier
Je kan een bestaand model gebruiken, dat getraind is op features van de meest voorkomende objecten in de wereld.

Hoe zwaarder het model dat je download, hoe beter de accuracy, en hoe meer objecten herkend worden.

**MobileNet**
https://github.com/tensorflow/models/blob/master/research/slim/nets/mobilenet/README.md

**ML5 Libraries**
Image:
- ImageClassifier
- PoseNet
- BodyPix
- UNET
- Handpose
- Facemesh
- FaceApi
- StyleTransfer
- pix2pix
- CVAE
- DCGAN
- SketchRNN
- ObjectDetector

Sound:
- SoundClassification
- PitchDetection
  
Text:
- CharRNN
- Sentiment
- Word2Vec

Helpers
- NeuralNetwork
- FeatureExtractor
- KNNClassifier
- kmeans


### Feature Extraction



## Les 3
*(opgenomen les: zie teams 2022-02-23)*

handpose, bodypose, face, object recognition

- PoseNet
- Facemesh
- FaceApi
- Handpose API
- ObjectDetector
- FeatureExtractor

Inspiration: 
http://charliegerard.dev  
https://unity.com/products/machine-learning-agents  
https://www.youtube.com/watch?v=mPbtR4vorgY  
https://code.visualstudio.com/docs/other/unity  


PoseNet vs imageClassifier

### PoseNet
https://learn.ml5js.org/#/reference/posenet

https://cmgt.hr.nl/project/danceflow
https://glitch.com/~draw-circle
https://github.com/ml5js/ml5-library/blob/main/examples/javascript/PoseNet/PoseNet_webcam/sketch.js
https://www.youtube.com/watch?v=DMebdxAp0j0
file:///C:/Users/lpsva/AppData/Local/Temp/PRG08-2022-WEEK3.pdf

### FaceApi
https://learn.ml5js.org/#/reference/face-api

https://www.youtube.com/watch?t=765&v=Hd6PG9R3r6c&feature=youtu.be

### Facemesh
https://learn.ml5js.org/#/reference/facemesh

### Handpose API
https://learn.ml5js.org/#/reference/handpose

landmarks

### ObjectDetector
https://learn.ml5js.org/#/reference/object-detector

### FeatureExtractor
https://learn.ml5js.org/#/reference/feature-extractor

### EmotionClassifier
https://brendansudol.com/writing/tfjs-emotions
https://www.codeproject.com/Articles/5276827/AI-Age-Estimation-in-the-Browser-using-face-api-an
https://www.codeproject.com/Articles/5276822/Pre-Trained-AI-Emotion-Detection-With-face-api-and



### Opdracht Week 3 Deliverable
https://github.com/HR-CMGT/PRG08-2021-2022/tree/main/week3

1. Bedenk een concept voor het werken met gezichtsuitdrukking herkenning, lichaamspose herkenning, handpose herkenning, object detectie, of de image feature herkenning uit week 2. (Dat is de imageClassifier waar je je eigen images aan hebt toegevoegd)
2. data uit met javascript en geef feedback aan de gebruiker via de UI.
3. Bouw een eenvoudige UI voor dit concept met HTML en CSS. De gebruiker hoeft dus niet in de console te kijken.

## Machine Learning Explained in 100 Seconds
https://www.youtube.com/watch?v=PeMlggyqz0Y

Machine Learning is the process of teaching a computer how perform a task with out explicitly programming it. The process feeds algorithms with large amounts of data to gradually improve predictive performance. 

### Goals
Classification
Prediction (Regression)

### Data
Aquire Data
Better data > better results (Garbage in Garbage out)

Data scientist

Feature engineering

Dataset:
- Training set
- Test set

### Algoritms

Linear Regression
Decision Tree
Convolutional Neural Network 


Error Function (Loss function)
Classification: Accuracy
Regression: Mean Absolute Error

Languages:
Python
R
Julia

Frameworks:
NumPy
scikit learn
PyTorch
Tensorflow
Pandas

### Model

Input > Prediction

Can be embedded or deployed to cloud.

## TensorFlow.js Quick Start
https://www.youtube.com/watch?v=Y_XM3Bu-4yc

Webbased Machine Learning

https://playground.tensorflow.org
https://www.kaggle.com/jeffd23
https://developers.google.com/machine-learning/crash-course/

Dataset MNIST
https://ml4a.github.io/demos/confusion_mnist/