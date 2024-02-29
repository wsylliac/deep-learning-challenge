# Report on the Neural Network Model: Charity Funding Predictor 

## Overview 

Alphabet Soup, a non-profit organization, aims to develop an algorithm for predicting the success of funding applicants. Leveraging machine learning and neural network techniques, we aim to utilize the dataset's features to construct a binary classifier. This classifier will determine whether applicants funded by Alphabet Soup are likely to succeed or not.

## Results 

To initiate the data processing, I removed any irrelevant information. After excluding 'EIN' and 'NAME', the remaining columns were designated as features for the model. 'NAME' was reintroduced in the second phase for binning purposes. Subsequently, the data was divided into training and testing sets. The target variable for the model, labeled "IS_SUCCESSFUL," was assigned values of 1 for "yes" and 0 for "no." Analysis of the APPLICATION data involved using the "CLASSIFICATION" value for binning. I established cutoff points using multiple data points to group "rare" variables together and assigned them the new label "Other" for each unique value. Categorical variables underwent encoding using `get_dummies()` after confirming the success of binning.

## Data Processing 

1. What variable(s) are the target(s) for your model?

The 'IS_SUCCESSFUL' column from the application_df DataFrame serves as the target variable.

2. What variable(s) are the features for your model?

The feature variables comprise every column except 'IS_SUCCESSFUL' from the application_df DataFrame, as determined by excluding the 'IS_SUCCESSFUL' column from the original DataFrame.

3. What variable(s) should be removed from the input data because they are neither targets nor features?

Both the 'EIN' and 'NAME' columns were excluded from the dataset as they neither serve as target variables nor feature variables.

## Compiling, Training, and Evaluating the Model

Each model utilized three layers in total following the application of Neural Networks. The quantity of hidden nodes was determined by the number of features available.

* How many neurons, layers, and activation functions did you select for your neural network model, and why?

Initially, I selected 8 nodes for the first hidden layer (hidden_nodes_layer1) and 5 nodes for the second hidden layer (hidden_nodes_layer2) as arbitrary starting points. These values were chosen with the intention of refining them through subsequent iterations.

* Were you able to achieve the target model performance?

It managed to attain the model accuracy of 78%.

* What steps did you take in your attempts to increase model performance?

    * Introduced additional layers
    * Eliminated more columns
    * Increased the number of hidden nodes
    * Adjusted the activation functions for each layer. 


## Summary

In general, the deep learning model achieved an accuracy of approximately 78% in predicting the classification problem. Employing a model that exhibits stronger correlation between input and output variables would likely lead to increased prediction accuracy. This could involve conducting additional data preprocessing upfront and selecting a model with alternative activation functions. Continuously iterating and fine-tuning the model parameters until higher accuracy levels are attained would also be beneficial.