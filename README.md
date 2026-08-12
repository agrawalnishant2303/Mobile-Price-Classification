# Mobile Price Classification

a. **Problem Statement**: The objective of this project is to build a **machine learning classification model** capable of predicting the price range of a mobile phone based on its hardware specifications (such as RAM, battery power, and camera quality).

b. **Dataset Description**:

- Source - Kaggle (https://www.kaggle.com/datasets/iabhishekofficial/mobile-price-classification)
- Dataset Size - 2000 records (balanced dataset )
- Features - 20 independent features like ram, cpu, etc..
- Target Variable - price_range (Multi-class classification problem: 0, 1, 2, 3 representing low, medium, high, and very high cost)

c. **GitHub Repository Link**: https://github.com/agrawalnishant2303/mobile-price-classification.git

d. **Models used**:

|    ML Model Name    | Accuracy |   AUC    | Precision |  Recall  |    F1    |   MCC    |
|:-------------------:|:--------:|:--------:|:---------:|:--------:|:--------:|:--------:|
| Logistic Regression |   0.94   | 0.993989 |  0.93727  | 0.936574 | 0.93645  | 0.920027 |
|    Decision Tree    |  0.835   | 0.887603 | 0.831899  | 0.829916 | 0.829491 | 0.780168 |
|    Random Forest    |  0.8925  | 0.982648 | 0.891633  | 0.891418 | 0.890548 | 0.857154 |
| K-Nearest Neighbors |  0.4175  | 0.67377  | 0.445406  | 0.414818 | 0.41618  | 0.231344 |
|     Naive Bayes     |  0.7975  | 0.95597  | 0.798332  | 0.79258  | 0.792928 | 0.731329 |

e. **Model Observations**:

| ML Model Name                    |                                                                                                                                                    Observation about model performance                                                                                                                                                    |
|:---------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| Logistic Regression              |                                            This model performed **exceptional** on the dataset indicating highly linear relationship between the features and the target variable price range. This was able to efficiently separate the four classes with an **accuracy** of around **94%**.                                             |
| Decision Tree                    |                                          This model was able to capture the linearity between the features and form the primary decision boundary but suffered a loss during testing due to **overfitting** on training data and hence was able to achieve an **accuracy** of around **83.5%**.                                           |
| Random Forest                    |                             Since this is an **ensemble** model, it was able to successfully aggregate multiple decision trees to reduce variance and hence **preventing overfitting** on the training data. It achieved an **excellent AUC** of more than **98%** significantly outperforming decision tree.                             |
| K-Nearest Neighbors              | **Curse of dimensionality** is correctly being proved for this model since it has the **least accuracy** of only around **40%** struggling significantly on training as well as test data. The importance of strong predictors like ram was heavily diluted by less relevant features since it calculated distance using all 20 features. |
| Naive Bayes                      |                       This model had a **moderate performance** on the mobile price classification dataset achieving an **accuracy** of around **80%** since Gaussian Naive model assumes all features are **independent** but we observed moderate correlation between the features hence capping its performance.                       |
| Overall Winner for your dataset? |                                                                                          Since the selected had a highly linear relation with the target variable **Logistic Regression** is clear winning model with an accuracy of around 94%.                                                                                          |