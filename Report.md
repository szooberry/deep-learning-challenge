## REPORT

### Overview
The purpose of this analysis is to create a deep learning neural network that can take data from the Alphabet Soup Charity pertaining to grants offered to applicants, and predict if the respective charitable venture will be successful or not.

### Results
#### Data Processing
1. What variable(s) are the targets of your model?

The only target variable of the model is the IS_SUCCESSFUL data column as that pertains to if the charitable venture was successful

2. What variable(s) are the features for your model?

- NAME
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- INCOME_AMT—Income classification
- ASK_AMT—Funding amount requested

Are all feature variables for the model

3. What variable(s) should be removed from the input data because they are neither targets nor features?
- EIN
- STATUS—Active status
- SPECIAL_CONSIDERATIONS—Special considerations for application

These columns were all removed and were neither featues nor a traget for the model


#### Compiling, Training, and Evaluating the Model
1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
- Input layer: 80 neurons with ReLu activation function
- 1st Hidden Layer: 40 neurons with Sigmoid activation function
- 2nd Hidden Layer: 40 neurons with ReLu activation function
- 3rd Hidden Layer: 40 neurons with TanH activation function
- 4th Hidden Layer: 20 neurons with ReLu activation function
- Output layer: 1 neuron with Sigmoid activation function

2. Were you able to achieve the target model performance?
I was not able to achieve the target of 75% accuracy, but got quite close by increasing the number of epochs

3. What steps did you take in your attempts to increase model performance?
I removed the Status and Special considerations columns, binned all other categorical data columns by introducing an "Other" category, binned the income_amt column into low, mid and high income categories, and also reinstated the Name column by binning the less frequent applicants separately from the top applicants. 

Reintroducing the name feature was the most effective at improving accuracy, but exposes the model to overfitting.


