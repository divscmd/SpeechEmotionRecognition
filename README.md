# Speech Emotion Recognition

## Overview

This project is part of the CodeAlpha Machine Learning Internship.

The goal of this project is to recognize human emotions from speech audio using
Machine Learning and Deep Learning techniques.

The project uses the RAVDESS (Ryerson Audio-Visual Database of Emotional Speech
and Song) dataset. Audio signals are converted into MFCC (Mel-Frequency
Cepstral Coefficient) features and classified using a 1D Convolutional Neural
Network (CNN).

## Dataset

Dataset: RAVDESS Emotional Speech Audio

Source:
https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio

The dataset contains 1,440 audio files across 8 emotion categories:

- Angry
- Calm
- Disgust
- Fearful
- Happy
- Neutral
- Sad
- Surprised

The dataset contains fewer Neutral samples than the other emotion classes.

## Methodology

The project follows these main steps:

1. Download the RAVDESS dataset from Kaggle.
2. Load and organize the audio files.
3. Extract MFCC features from each audio file.
4. Normalize the MFCC features.
5. Split the dataset into training and testing sets.
6. Train a 1D Convolutional Neural Network.
7. Evaluate the model using accuracy, precision, recall and F1-score.
8. Visualize the confusion matrix and sample predictions.

## Feature Extraction

MFCC features were extracted using Librosa.

Configuration:

- Sample rate: 22,050 Hz
- Number of MFCC features: 40
- Fixed time frames: 174

The resulting MFCC representation was converted into the format:

```text
(samples, time frames, MFCC features)
