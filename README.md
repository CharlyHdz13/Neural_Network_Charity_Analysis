# Neural Network Charity Analysis
## Overview of the analysis
In the following analysis, we want to determine if an applicant for a fund will be succesful or not. This will be achieved through the building of a neural network. The neural network will be trained with data collected from over 34,000 organizations from the past who have been funded. The data first was processed before feeding it two our neural network. We transformed any categorical data that we had into numerical data and tried our best to avoid skewness. In the next section the results are shown.
## Results
- _Data Preprocessing_
    - We are interested in seeing if an application will be successful or not, therefore from our dataset the target variable for our model will be `IS_SUCCESSFUL`.
    - The `EIN` and `NAME` are only identification variables, these don't bring any type of value to our model. These are removed and the remaining variables in our dataset are the features of our model.
- _Compiling, Training, and Evaluating Model_
    - To start we want a deep neural network for a good classification, but we don't want to overfit. So our first network is built as follows:
        - 2 Hidden Layers
        - First layer has 80 neurons, with `Relu` as the activation function
        - Second layer has 30 neurons, with `Relu` as the activation function
        - Output layer has `Sigmoid` as the activation function

    The reason behind the 80 neurons is because we have a total of 43 features, therefore we are choosing approximately the double of neurons for our first hidden layer. The activation functions for the first and second layer were chosen because this have worked pretty good for classification operations in the past. The output layer uses the `Sigmoid` activation function because we want only to know if the application was succesful or not, we are looking for a binary result, and this function gives us that.
   
   
## Summary
