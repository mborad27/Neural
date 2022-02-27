# Neural Network Charity: Deep Learning
## Overview
Becks is a data scientist and programmer for Alphabet Soup, a nonprofit foundation dedicated to helping organizations that protect the environment, improve people's well-being, and unify our world.They have raised and donated over 10 billion dollars in the past 20 years. This money has been used to invest in lifesaving technologies and organize reforestation groups around the world.

From Alphabet Soup's business team, Becks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization. We will be helping Beck understand neural networks and design and train these models using Python TensorFlow library. This model will help Alphabet Soup determine which organizations should recieve donations.
## Results
**Data Preprocessing**
* The IS_SUCCESSFUL column is considered the target for my model.
* The APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and ASK_AMT columns are considered to be the features of my model.
* The EIN, NAME, STATUS, and SPECIAL_CONSIDERATION columns are neither targets nor features and should be removed from the input data.
* Below is the code that preprocesses the data:
![Capture](https://user-images.githubusercontent.com/92230478/155866615-91e8d07b-0ff6-4d3d-be9f-8bd6f6739a6e.PNG)

**Compiling, Training, and Evaluating the Model**
* I selected 120 neurons with a sigmoid function for my first layer, 50 nuerons with a ReLU function for the second, and 18 neurons with for the third, and a sigmoid function for the outer layer. I chose to change the activation function for the first layer because it increased the model's performance.
* I only achieved an accuracy of 69% and was not able to achieve the target model performance.
* I tried to increase the model performance by dropping more columns, creating more bins for rare occurances in columns, decreasing the number of values in some bins, adding more neurons to the hidden layers, using a differnet activation function, and increasing the number of epochs.
* Below is the code for desiging the model and creating a callback that saves the model's weights every 5 epochs:
![Capture1](https://user-images.githubusercontent.com/92230478/155866689-d39b2265-f525-45cd-aa83-38cc747f76b8.PNG)
![Capture2](https://user-images.githubusercontent.com/92230478/155866693-2e142174-5fac-4be9-81b8-f4b2711acb22.PNG)

## Summary
Through the removal of noisy features, additional neurons and hidden layers and changed activation functions, the accuracy of my optimized model for predicting whether a donation is successful ended up being 0.6868 and its loss metric was 1.3676.

A random forest model could solve this classification problem by randomly sampling the preprocessed data and building several smaller, simpler decision trees. Some benefits of using a random forest model include how robust it is against overfitting of the data because all of the weak learners are trained on different pieces of the data, it can be used to rank the importance of input variables, it is robust to outliers and nonlinear data, and it can run efficiently on large datasets.
