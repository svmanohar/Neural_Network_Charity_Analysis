# Neural Network Charity Analysis

## Overview

The purpose of this analysis is to create a neural network for redistribution that can take an input of a series of data surrounding organizations' grant applications, and predict which applicants would be successful if funded by our parent organization; in other words, **how effective is our investment on the business outcome?**

## Results

### Data-Preprocessing

- Our target variable was the "IS_SUCCESSFUL" column, which is the historic data showing whether the organization that was funded was ultimately successful from a business perspective
- Application Type, Organization Classification, Use Case, Organization Type, Income Classification, the presence or lack of special considerations, and actual funding amount were all features in our analysis
- The organization name and ID were not valuable features from the outset and were dropped during preprocessing

### Compiling, Training, and Evaluating the Model

- Following the rule of 3, we chose a total of 43 neurons for our input layer, as this was the number of inputs in our model. We then used three hidden layers using the relu activation function, each having (3*43 = 129) neurons

- Unfortunately, our model, without optimization, was not able to reach a target threshold of 75% accuracy

- I attempted to optimize the model by increasing the initial hidden layers from 2 to 3, binned additional data in the Income Classification column, and attempted to increase the number of training epochs to 200 from 100. None of these efforts increased the model accuracy from 73% to the target 75%

### Summary

Overall, our model was able to predict the IS_SUCCESSFUL status of an organization funded by our parent granting organization with approximately 73% accuracy, below our target threshold of 75%.

In order to isolate whether this network needed further optimization, I would attempt to construct a Random Forest model and run the same analysis, comparing the resultant accuracies.