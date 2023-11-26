# Using Google Colab, TensorFlow, and Keras to design a deep learning model to evaluate nonprofit foundation funding opportunities

Contributor: Brian Kath

## Repository Structure

- Main Folder

  - .gitignore
  - AlphabetSoupCharity.ipynb
  - AlphabetSoupCharity_Optimization.ipynb
  - README.md

## Overview

For this project, I used Google Colab, Python, Pandas, scikit-learn, TensorFlow, and Keras to design a deep learning model to evaluate data to determine the best funding opportunities for a fictional nonprofit foundation.

The first part of the project, was to preprocess the data. I first imported a CSV file containing more than 34,000 orginations that have received funding from the fictional nonprofit into a Pandas DataFrame. I then reduced the data to desirable columns and broke the data up into the target and feature portions for the model. Then I preprocessed the data into a training and testing dataset, and I used StandardScaler to scale the training and testing data.

The second part was to compile, train, and evaluate the deep learning model. For this, I used TensorFlow to design a neural network by creating a binary classification model that can predict if one of the nonprofit funded orginizations will be successful based on the features in the dataset. First, I created the neural network by assigning the number of input features and nodes for each layer using TensorFlow and Keras. I then added two hidden layers to try and increase the performance and complexity of the neural network. Next, I added an output layer to help produce the desired final prediction. Finally, I exported the results as an HDF5 file.

The third part of the project was to try and optimize the original model. For this, I tried several variations on the original model to see if I could identify a better design for the neural network. I tried dropping additional columns from the original data, both increasing and decreasing the number of values for each bin, and adding more neurons to my hidden layers. None of these approaches appeared to have much of an impact on the predictive accuracy of the model.

The last part of the project was to write a report on the neural network model. The report is below:

### Overview

The purpose of the analysis was to create a neural network to determine whether funding applicants will be successful if funded by the fictional nonprofit.

### Results

- Data Preprocessing

  - The target variable for the model was the IS_SUCCESSFUL column of the data.
  - The feature variables for the model were every other column in the data except columns EIN and NAME.
  - The EIN and NAME columns were removed from the input data because they were determined to be neither target nor features.

- Compiling, Training, and Evaluating the Model
  - For the neural network, I chose 9 neurons, 2 hidden layers, and 2 different activation functions because I thought that would be optimal for the desired outcome.
  - I was not able to achieve the target model performance of 75% by adjusting the model.
  - In trying to increase the model performance, I tried adjusting the number of neurons, narrowing down the data used, and increasing the number of nodes per hidden layer.

### Summary

The overall results showed a relatively well performing model. Some additional ways to try and increase the model performance could be further adjustments to the number of columns from the original data used, creating more bins for rare occurrences in columns, increasing or decreasing the number of values for each bin, adding more neurons to the hidden layers, adding more layers, using different activation functions, or adding or reducing the number of epochs to the training regimen.
