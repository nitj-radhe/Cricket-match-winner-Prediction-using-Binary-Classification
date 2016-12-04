# Cricket-match-winner-Prediction-using-Binary-Classification

## Synopsis
The problem objective is to predict the winner of the cricket match based on the observations given in the dataset. The dataset consists of 28 features which are observed during the match. The approach used in modeling the Prediction system is logistic Regression classifier. The reason behind choosing the logistic regression classifier over the neural network is that the number of samples in the dataset are 252 samples with 28 features set for the each example. Choosing the neural network over logistic regression may overfit the model and 


## Data Preprocessing and Model Design.
The observation of the dataset given shows some of the factors which can be neglected.In this example we are neglecting the two features which are Data and Time of the match.The dataset consists of the 28 featurs as the input and the output as binary values assigned predicting the winner of the match based on these feature set. The values are assigned as team 1=1 and team 2=0 for the winning team as true labels.The dataset preprocessing for this problem statement is as follows:
Markup:1. Load the Data
	2. Extract the features  (Neglect less contributing factors)
	3. Feature slection using PCA
	4. Class_weight vector calculation based on the occurance of each example in the dataset.
Extracting the features.The following conditions and modifications are applied to the dataset.As the model learns accordingly to the feature set and all the examples are assigned accordingly, it is valid to assign the values.assuming that the home match favours the home team the values are assigned accordingly t that of home ground and some venues are away match for both the playing team in that case the value is assigned to -1.
		1. Team1 is set to the value 1 and Team2 is set to the value 0
		2. City values are assigned accordingly to that of the team factor.
		3. Time and date factors are neglected assuming that there is not much variance in the feature. 
Dimension Reduction Using Principle Component Analysis Considering all the features set initially, doing PCA and then finding the variance plot for the set. Further on observing the variance plot we can see that 99.4 of the data varince can be observed in 23-24 features axis. So further reducing the dataset to 23 axis.
The 80% of the dataset is assigned to the training set and 20% is assigned to the test dataset.


## Prerequisities
The following softwares/Libraries are the prerequities for testing the model.
		1.python 2.7
		2.Matplotlib
		3.sklearn
		4.pandas
		5.numpy

## Logistic Regression Model
The logisitic Regression classifier Model is used to train the dataset for classification, The parameters considered are C(Regularisation factor) where smaller the value, gives stronger regularisation. Number of iterations and class_weight factor for smooth modelling of dataset.
The model parameters which are need to be changed then cosidering them as default are the regularisation factor,number of maximum iterations and class weight values.
The class weight values are assigned in consideration of number of times the samples of the each class observed in the dataset. The class weight factors are the one which effect the weights during the training of the model.


## Results
The observation over the ROC curve shows that the model has learnt the parameters perfectly. The model is tested over the test data and observed to give the over all accuracy of 94.1% .The followng precision,recall and F1 score values are as follows 

                          precision    recall  f1-score    support
          class negative     1.00      0.88      0.94        26
          class positive     0.89      1.00      0.94        25
          avg/total          0.95      0.94      0.94        51
         
         Accuracy = 94.1%
