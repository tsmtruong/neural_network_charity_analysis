# Neural Network Charity Analysis

## Overview
The purpose of this analysis was to use deep-learning neural netowrks to analyze and classify charitable donations and their rate of success. To do this analysis we used Tensorflow in python as well as SciKitLearn. We performed preprocessing on the data, compiled, trained and evaluated the model, as well as performed optimizations.

## Results

### Data Preprocessing
- The column IS_SUCCESSFUL contains binary data refering to weither or not the charity donation was used effectively. This variable is then considered as the target for our deep learning neural network.
- The following columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are the features for our model. Encoding of the categorical variables, spliting into training and testing datasets and standardization have been applied to the features.
- The columns EIN and NAME are identification information and have been removed from the input data as they do not add value to the model.

### Compiling, Training, and Evaluating the Model

- This deep-learning neural network model is made of two hidden layers with 80 and 30 neurons respectively. The input data has 43 features and 25,724 samples. The output layer is made of a unique neuron as it is a binary classification. To speed up the training process, we are using the activation function ReLU for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer. For the compilation, the optimizer is adam and the loss function is binary_crossentropy.
- The model accuracy was under 75%. This would not be considered a successful model performance for the charity donations.
- To increase the performance of the model, we applied bucketing to the feature ASK_AMT and organized the different values by intervals. We increased the number of neurons on one of the hidden layers, additionally we used a model with three hidden layers. We also tried a different activation function (tanh) but none of these steps helped improve the model's performance.

## Summary
Overall the neural network did not reach the target of 75% accuracy during any of the evaluation runs. When considering our model did not reach the target performance which was set at 75%, what many would consider an average level, we can confidently say that the model is not outperforming. In this specific situation I would possibly consider running a supervised machine learning model as we know which variable we want to test. We are also using a binary classification method in a supervised machine learning mdoel we could pair that wirh Random Forest Classifier to give the model a higher chance of success.
