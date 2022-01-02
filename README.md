# Neural_Network_Charity_Analysis

## Overview

The purpose of this analysis is to be able to predict in the future if an applicant will be successful after being funded by Alphabet Soup. This prediction is done by performing a neural network model using historical data from previous funding.

## Results

### Data Preprocessing

-	The target variable for this model is the “IS_SUCCESSFUL” column, which contains information about whether the account receiving Alphabet Soup’s funding was successful (1) or not (0).
-	The variables that were considered to be features for the model were the applicant’s application type, affiliation, classification, use case, organization type, income amount, and ask amount.
-	After optimization, the variables that were not considered to be features for the model and were removed from the input data included the name of the organization, their EIN, their account status, and whether or not they have special considerations.

### Compiling, Training, and Evaluating the Model

-	I chose to use a total of 18 neurons, since the rule of thumb is to use 2-3 times the number of inputs. In this case, there were 7 inputs so I used ~2.5 times 7 equals 21 neurons. I used two hidden layers with relu activation functions because this is the default recommendation for modern typical models and other activation functions proved to be less accurate. Lastly, I used a sigmoid output activation function because it is the best option when the output is binary, which is the case in this model.
-	No, I was not able to achieve the target model performance but I got closer with an accuracy of 72.8%.
-	In order to attempt to achieve the target model performance of 75% I first tried several combinations of adding/subtracting the number of neurons, the number of hidden layers, and the number of epochs. The second thing I tried was using various combinations of hidden layer and output activation functions. Neither of these attempts improved the performance of the model. Finally, I eliminated one column at a time to determine the variables that hindered the performance of the model. I determined that two variables in particular helped improve the performance of the model, and even further when they were eliminated together. These two variables included the account status and special considerations columns. This makes sense as the status column only had 5 rows with a status of “0” and the special considerations column only had 27 rows with the label “Y”. One thing that could be done to make this model even more effective would be to eliminate outliers. The affiliation, use case, and organization columns all contained outliers that could be hindering the model. More research and trials would need to be performed to test this out and effectively eliminate the outliers.

## Summary

Overall, this neural network model did not quite meet expectations. The goal was to have an accuracy of over 75% and I was only able to achieve just under 73% with this model. It’s possible that 75% could be achieved as mentioned previously, but even at 75% the accuracy is not great, and another model could be better suited for achieving an even better accuracy.

I recommend trying a random forest model for this dataset. I believe it’s too complicated for a multiple linear regression or SVM model, but a random forest would provide for faster process times and is robust enough to handle the amount of data. 
