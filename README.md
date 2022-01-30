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
        The accuracy of this model was of 0.727 and in the following tests we are looking to improve it.
    - Test 1: Increasing the number of hidden layers
        - 3 Hidden layers
        - First layer has 80 neurons, with `Relu` as the activation function
        - Second layer has 30 neurons, with `Relu` as the activation function
        - Third layer has 10 neurons, with `Relu` as the activation function
        - Output layer has `Sigmoid` as the activation function
        
        The accuracy of this model was of 0.725, no improvement.
    - Test 2: Increasing the number of neurons per layer
        - 2 Hidden layers
        - First layer has 130 neurons, with `Relu` as the activation function
        - Second layer has 65 neurons, with `Relu` as the activation function
        - Output layer has `Sigmoid` as the activation function
        
        The accuracy of this model was of 0.725, no improvement.
    - Test 3: Using `Tanh` as activation function instead of `Relu`
        - 2 Hidden layers
        - First layer has 80 neurons, with `Tanh` as the activation function
        - Second layer has 30 neurons, with `Tanh` as the activation function
        - Output layer has `Sigmoid` as the activation function
        
        The accuracy of this model was of 0.726, no improvement.
        
    - We were not able to achieve the target perfomance of 0.75, but still there is lots of improvement to be made on this first model.
    - Three different approaches were made to try to improve the model: increasing number of hidden layers, increasing number of neurons per layer and using a different activation function.
## Summary
From all the results we get that at with those specific modifications there is no great improvment in the accuracy of our model. Perhaps some combinations of the three or lookin into how we binned certain features might to the trick. Regardless of that the model is good to have a first impresion of the applicant. Also I would take a look into building a model using Random Forest, due to the fact that our data is tabular and we could have the same accuracy with better performance. 
