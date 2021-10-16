# Neural_Network_Charity_Analysis

## Overview
- Use a neural network/deep machine learning to create a classification system capable of predicting whether applicants will be successful if funded by Alphabet Soup. 

## Resources
- VS Code (v 1.61), Python 3.7.11
- Data provide via csv/charity_data.csv

## Results
- Data Preprocessing
	- The target for this model is the 'IS_SUCCESSFUL' column.
	- The features are the 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS' & 'ASK_AMT' columns.
	- The columns that should be removed are the "EIN" & "NAME".
- Compiling, Training, and Evaluating the Model
	- The model has 2 layers.  The first layer had 80 neurons (between 2 and 3 times the number of inputs).  The second layer had 30 neurons.  The relu and sigmoid functions were chosen for this model.  Relu was used due to the lack of negative numbers and sigmoid was used on the output layer because desired output was between 0 and 1.
	- This model was not able to achieve the target of 75% accuracy.
	- Accuracy of Original Model
	
	![Accuracy of Original Model](https://github.com/jediracer/Neural_Network_Charity_Analysis/blob/main/images/Original_Accuracy.png)
	
	- I attempted to increase the accuracy of the model by:
		- removing the 'STATUS', 'INCOME_AMT' & 'SPECIAL_CONSIDERATIONS' columns during preprocessing.
		- changed the binning parameters for 'APPLICATION_TYPE' & 'CLASSIFICATION'.
		- added a third layer to the model.
		- changed the number of neurons in each of the 3 layers.
		- reduced the number of epochs.

## Summary
- The accuracy of the original and "optimized" models did not meet or exceed the target accuracy of 75%.  The "optimized" model had a lessor accuracy than the original.  After trying different combinations of number of layers, number of neurons, activation functions, binning parameters & removal of additional columns, I believe additional data would be needed to achieve and accuracy of 75% or greater. 