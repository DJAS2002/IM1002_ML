# IM1002_ML
Machine learning, gaze estimation with Google MediaPipe using SVM, K-Nearest Neighbor, Decision Tree and Random Forest classifiers.

Before running Notebook 2 and later please unzip data.zip to a local folder ./data

## Notebook 1
### POSE Landmark acquisition and storage

This notebook is designed to capture video and detect the pose using MediaPipe
It wil capture poses of action = [TL, TR, BL, BR, CENTER]  and store it into a (directory) structure:
persoon_xxxx/action/sequence_nr/frame_nr.npy
where xxxx is the persons ID, sequence is a series of frames and sequence_nr and Frame_nr are the corresponing ID's of the instances.

## Notebook 2
### Data and feature evaluation

1. Visual inspection of data by creating an video of all acquired landmarks and features
2. Distribution of the features
3. Pairplots


## Notebook 3
### PCA Analyses
The aim is to see what the principle components of the data set are

## Notebook 4
### MODEL training and hyper parameter search

This notebooks trains the models SVM, KNN, DT and RF
- it normalizes the data to 0.0 mean and 1.0 sigma
- trains the models with the default values of scikit learn
- trains the models with the default values of scikit learn using PCA feature reduction
- Grid and random searches for best hyper parameters

It displays scores:
- F1 scores 
- Recall 
- Precision
- confusion matrices

## Notebook 5
### Testing pose estimate with webcam

Loads one of the models trained, grabs a live datastream from the webcam and predicts the gaze.
