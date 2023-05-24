# deep-learning-challenge

Overview
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

Results:

Data Preprocessing

What variable(s) are the target(s) for your model?
The target variable for this model is 'IS_SUCCESSFUL', which indicates whether the money was used effectively.
What variable(s) are the features for your model?
The feature variables for this model are every other variable in the dataset, after preprocessing. This includes 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', and 'ASK_AMT'.
What variable(s) should be removed from the input data because they are neither targets nor features?
The 'EIN' and 'NAME' variables were removed from the input data, as they are identification information and do not provide any useful patterns for the model.
Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?

The neural network model consists of six hidden layers with different numbers of neurons: 80, 30, 80, 30, 80, and 30 respectively. The model uses the ReLU activation function for hidden layers and the sigmoid function for the output layer. These choices are common for binary classification problems, with ReLU helping to handle the vanishing gradient problem and sigmoid ensuring output values between 0 and 1.
Were you able to achieve the target model performance?

The model did not initially achieve the target model performance. Therefore, further steps were taken to optimize it.
What steps did you take in your attempts to increase model performance?

In an attempt to increase model performance, the following steps were implemented:
Additional hidden layers were added to help the model find more complex patterns in the data.
Batch normalization was added to standardize the inputs to each layer, helping the model train more effectively.
Dropout layers were introduced to reduce the risk of overfitting.
The learning rate was reduced over time, allowing the model to fine-tune its weights more precisely as training progressed.
After these changes, the model was trained and evaluated again.

Summary:

In the implemented deep learning model, various optimization techniques were applied, such as the addition of extra hidden layers, the use of batch normalization, and dropout layers, as well as learning rate decay. Despite these efforts, the desired accuracy of 75% was not reached.

A different approach might involve using a different type of machine learning model. For instance, a Gradient Boosting Classifier, known for its efficiency with both categorical and numerical data, could potentially deliver better results in this classification problem. By combining weak learners, Gradient Boosting effectively reduces bias and variance, making it a powerful candidate to consider for this task.

Ensemble methods, which amalgamate the decisions from multiple models, could also be a promising approach. They can leverage the strengths of different models while mitigating their weaknesses, often leading to higher predictive accuracy. However, this approach requires significant computational resources and may take more time to train.
