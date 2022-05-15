# Neural_Network_Charity_Analysis
## Overview of the analysis
The purpose of this project was to create a binary classifier that is capable of predicting whether applicants will be successful if funded by the company Alphabet Soup.

The received CSV contains more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectivel


# Data Preprocessing
## What variable(s) are considered the target(s) for your model?
* The target variable for the model was the "IS_SUCCESSFUL" category.
* ![image](https://user-images.githubusercontent.com/96098938/168474330-6835ee1c-ebcb-4b47-ac23-83295b1d9ecf.png)

* What variable(s) are considered to be the features for your model?
  The original model considered the following columns as features: EIN, NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT,  SPECIAL_CONSIDERATIONS, ASK_AMT, IS_SUCCESSFUL.
* What variable(s) are neither targets nor features, and should be removed from the input data?
    For the original model we removed the EIN and NAME columns.

## Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model?
* The original model contained 2 layers with 30 and 25 neurons in each layer. The activation function is relu for hidden layers and output function is sigmoid. This model is approximately 72% accurate with loss of 57%.
![image](https://user-images.githubusercontent.com/96098938/168475350-7ff45a3b-cb46-495e-8883-6e4786da064a.png)

* Were you able to achieve the target model performance?
    * After all the modifications, I was not able to achieve target pergformance of 75%.
* What steps did you take to try and increase model performance?
  * Dropped more noisy data (columns AFFILIATION and SPECIAL_CONCIDERATION)
  * Attempt 1. Increased number of layers in the model from 2 to 3
 ![image](https://user-images.githubusercontent.com/96098938/168475018-c2585e19-eca3-4e5f-9c68-c0f0f32265f5.png)


  * Attempt 2. Adjusted the amount of neurons.  The neurons on the first layer were adjusted to 70, the second layer 35 and an added third layer with 25.
  * ![image](https://user-images.githubusercontent.com/96098938/168475029-12a8bd5b-a604-4cf9-a57e-03e88d3670af.png)

  * Attempt 3. The output layer was changed from "sigmoid" for all layers. 
  * ![image](https://user-images.githubusercontent.com/96098938/168474957-73d0b7e4-19fd-4c22-93d2-28bca7f8f7f1.png)

## Summary
The deep learning models failed to reach its target accuracy at 75%. The attempts to optimize the model also failed to reach the target of 75%. THe combined attempts to optimize only slightly decreased the accuracy of the original model. 

The variables we're working with could be researched further. For example the ASK_AMT has 8,747 unique values. It could be possible to dig deeper into these amounts and create bins for ranges. This would decrease the amount of unique values and may improve the overall accuracy of the model as well.
