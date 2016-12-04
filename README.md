# Cricket match winner prediction using the Logistic Regression classifier

## Synopsis
The problem objective is to find the winner of the cricket match based on the observations given in the dataset. The dataset consists of 28 features.

## Data Preprocessing 
The dataset contains 2000 features for each input and the size of the dataset is 62,In this classfication task,The Multi level perceptron model is used to predict the class of tumor present or not. The positive samples are assigned to the output 1 and the negative samples are assigned to value 0.
The features set is decreased to set of 6 features by appplying Principal Component Analysis based on combined features selection by selecting the 10 best features with means are more impact on the output and PCA the dataset on the 6 axis.
The 80% of the dataset is assigned to the training set and 20% is assigned to the test dataset.

## Prerequisities
The following softwares/Libraries are the prerequities for testing the model.
python 2.7
Matplotlib
sklearn
pandas
numpy

## Neural Network Model
The multi level perceptron model is used to classify the model,the specification of the model are solver of stocastic gradient decent with adaptive learning rate having the two hidden layers with one having of 15 neurons and the other with the 200 neurons.The initial learning rate is set to 0.01

## Results
The observation over the task is noticed that the model stops after certain specific number of iterations if there is not much change in the training loss and the training loss converges over the time. The model is tested over the test data and observed to give the over all accuracy of 85% bust as the dataset is skewed towards one class(having much of samples belonging to single class) The followng precision,recall and F1 score values are as follows 

                          precision    recall  f1-score    support
          class negative     1.00      0.75      0.86        12
          class positive     0.75      1.00      0.86         9
          avg/total          0.89      0.86      0.86        21
         
         Accuracy = 85.7%

# Cricket-match-winner-Prediction-using-Binary-Classification
