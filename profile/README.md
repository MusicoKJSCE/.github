## Hi there 👋

# Musico - Music Recommendation System

## Team Members
- [Dhruv Solanki](https://github.com/Dhruvsolanki345)
- [Anurag Singh](https://github.com/heyanurag)
- [Umang Thadani](https://github.com/thadaniumang)
- [Aayush Kapoor](https://github.com/aayush-kapoor)

## Introduction
With the rise of digital content distribution, people now have access to music collections on an unprecedented scale. Commercial music libraries easily exceed 15 million songs, which vastly exceeds the listening capability of any single person. With millions of songs to choose from, people sometimes feel overwhelmed. Thus, an efficient music recommender system is necessary in the interest of both music service providers and customers. Users will have no more pain to make decisions on what to listen while music companies can maintain their user group and attract new users by improving users’ satisfaction. This music recommendation system also helps the users to listen to the music based on their mood using which, an angry person can calm himself down by listening to the recommended songs.

## Motivation
Many music streaming services, such as Pandora and Spotify, are developing high-precision
commercial music recommendation systems at the moment. These businesses make money by
assisting customers in finding appropriate music and charging them for the quality of their
recommendations. As a result, there is a thriving market for good music recommendation
systems.

## Scope of Project
- Music recommendation will be based on mood of the user which will be get from user’s
facial expression
- We will use an already existing streaming service in order to retrieve and play music as it is
not in the scope of the project to develop our own music streaming service. We decided to
use Spotify because of their extensive APIs and SDKs which are easy to use.
- Spotify also offers access to a large amount of audio feature data connected to the music
which we retrieve and use in the recommender system
- This music recommendation will be available through a web application where music will be
displayed to user based on their facial expression and their previous watch history to enhance
the search result.
- After selecting the music, user can play it on our web application

## Tech Stack
- Front End: ReactJS, Material UI
- Back End: DjangoREST
- Database: PostgreSQL
- Machine Learning: Tensorflow, Keras
- Computer Vision: OpenCV
- Music API: Spotify

## Background Work
Our project primarily relies on two main sections, face recognition and mood analysis and the
latter depends on the results from the former. Hence it is important to perform these tasks in an
efficient manner. We use “Haar Cascade” algorithm which is commonly used for Facial
Recognition. We obtained the dataset from the Kaggle Competition "Challenges in
Representation Learning: Facial Expression Recognition Challenge" for mood analysis.

### Face Detection using Haar Cascade Method
The "Haar Cascade" algorithm is a popular facial recognition algorithm. It has a low
computational cost, a fast algorithm, and good accuracy.
It works in four stages:
- Haar-feature selection: It is carried out in order to extract useful elements for the purpose
of identifying an object
- Creation of Integral Images: computing the difference of dark and light rectangular
sections is required to extract Haar-like features, Integral Images considerably minimize
the time required to execute this activity.
- AdaBoost Training: From all of the features, this algorithm finds the best ones.
- Cascade Classifier: It's a way for cascading progressively complicated classifiers like
AdaBoost, allowing negative input (non-face) to be swiftly discarded.

### Mood Analysis using Keras
There are 3 steps involved in classifying facial expressions.
- Data Preparation: It's worth noting that we had an additional tag of "Disgust" and “Fear”
in the original given dataset, in addition to the "Angry, Surprise, Happy, Sad, and
Neutral" that we have implemented in our project, the main issue will be that the
distribution of the Disgust label in the provided data is quite unbalanced, accounting for
an unusually low percentage. Because the obvious imbalance in data distribution will influence further neural network training, we re-classify all pictures with the "Disgust"
label into the "Angry" label. Also, “Fear” is irrelevant as far as music-recommendation is
concerned. It can be clubbed with “Sad” there is no difference in the mapping
- Model Preparation: This project began with a clear definition of our primary goal:
categorise provided grayscale images into one of five classifications. Naturally, the task
of image categorization brings us to the well-known Convolutional Neural Network
(CNN).
- Model Evaluation: We finally evaluate our model with the test data
