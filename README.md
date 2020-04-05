# Alphabet_Soup
Machine Learning

# Project Overview/Challenge
	- Import, analyze, clean, and preprocess a “alphabet soap dataset” classification dataset.
	- Select, design, and train a binary classification model.
	- Optimize model training and input data to achieve desired model performance.

# Resources
- Data Source: "charity_data.csv".
- Software: Python 3.6.9:: Anaconda, Inc., Jupyter Notebook, 6.0.2, sklearn.

# Summary
- Preprocessed the charity_data
	- Imported the dataset
	- removed columns, "NAME" and "EIN", that will not be used for analysis.
	- bucketed "APPLICATION_TYPE" and "CLASSIFICATION" columns to combine rare categorical data.
	- encoded categorical variables using one-hot encoding. 
	- merged the one-hot encoded features and dropped the originals.
	- split the preprocessed data into a training and testing datasets.
	- scaled the data using StandardScaler.
- Binary classification models
	- tried three models Deep Learning Model, Neural Network Model and Basic Neural Network Model
	- Deep Learning Model
		- tried 2 hiden layers (activation=relu) and output layer (activation=sigmoid) with hidden_nodes 1st layer=8, 2nd layer=6
			- the Deep Learning Model shows very low outcome: Loss: 0.690797222348761, Accuracy: 0.5343440175056458
			- tried increasing the hidden_nodes for optimization to 1st layer=50, 2nd layer=25
				- this did not improve the results
			- tried to increase the hidden_nodes more to 1st layer=50, 2nd layer=25, however this did not improve the model - Loss: 0.6909905942883505, Accuracy: 0.5343440175056458
			- increased the epochs from 100 to 500 and increased the layers to 80 and 60 - did not improve the model
				- changed to 100 epochs - Loss: 0.6908012354686726, Accuracy: 0.5343440175056458
	- One Neural Network Model
		- performed better acurracy score - Loss: 0.5832519899582377, Accuracy: 0.7130029201507568
	- Used Basic Neural Network Model
		- performed the best accuracy result with 73% - Loss: 0.5543036206679164, Accuracy: 0.7306122183799744
- I was not able to achieve the target model performance, higher than 75% with all three models. 
- The best model with accuracy score of 73% was Basic Neural Network Model. However I might implement leaky_relu as the dataset has negative values.


