# deep-learning-challenge

Homework Module 21 deep learning challenge

# Alphabet Soup Charity Funding Predictor


## Overview of the analysis:


This project aims to develop a binary classifier using neural network models for the fictional nonprofit foundation Alphabet Soup which wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With the dataset provided, a binary classifier was created to predict whether applicants will succeed if funded by Alphabet Soup.

The dataset received is a CSV containing over 34,000 organizations that have received funding from Alphabet Soup. Within this dataset are several columns that capture metadata about each organization, such as:

<img width="364" alt="image" src="https://github.com/cassiewyattlkn/deep-learning-challenge/assets/108894970/32466c01-701e-4673-8c5e-19c241203a91">

**Data Preprocessing**

Following iterations with different feature combinations, it became apparent that certain features held significant predictive power crucial for achieving the target model performance. Notable features include:

- NAME
- APPLICATION_TYPE
- AFFILIATION
- CLASSIFICATION
- USE_CASE
- ORGANIZATION
- INCOME_AMT
- ASK_AMT

Conversely, some features exhibited minor to negligible significance for model performance, including:
- EIN
- STATUS
- SPECIAL_CONSIDERATIONS

For this project, the target variable being predicted is "IS_SUCCESSFUL."

**Compiling, Training, and Evaluating the Model**

The Optimized Neural Network Model was constructed as follows:
- As a binary classifier, the sigmoid activation function was applied to the output layer, compressing outputs into a range from 0.0 to 1.0, representing probabilities.
- To streamline training time per epoch and considering the model achieved target performance early, fewer neurons were employed.
- The binary_crossentropy loss function, tailored for binary classifiers, was utilized, with metrics set to 'accuracy' to capture accuracies computed by the loss function in the history object.
- Training was capped at ten epochs, given the model's early attainment of target performance and marginal improvement in accuracy thereafter.
- A noteworthy enhancement to model performance involved reintroducing the NAME feature as an input during model optimization, resulting in a significant performance boost.

**Summary**

This project entailed the development of a binary classification model utilizing Neural Networks. Pre-optimization, model accuracy hovered around 73%. However, post-optimization, the target performance was realized with an accuracy exceeding 79%.

For future exploration, investigating other well-performing binary classification algorithms, such as logistic regression, Naïve Bayes, and k-Nearest Neighbor, is envisioned. Comparative analysis against the optimized neural network model could provide valuable insights into model performance across different machine learning methodologies.
