# News Categorizer: NLP's Quest to Sort Meneame.net News 📰🏷🕶

## Introduction 🧐
The project focuses on Natural Language Processing (NLP) and aims to classify news articles from the meneame.net dataset. The dataset contains 177,000 news articles, and the goal is to create a model that can accurately classify articles into specific categories. The dataset suffers from class imbalance, with one category dominating the data. Four relevant classes, including technology, leisure, current news, and culture, are selected for classification. Text normalization techniques are applied to clean the data, and it is split into training and test sets.

## Techniques:🔮
Feature extraction is performed using sparse vector models such as Bag of Words and TF-IDF. Various classifiers, including Logistic Regression, Multinomial Naive Bayes, and Decision Trees, are trained on the extracted features. The models are evaluated using the F1 Score, which considers precision and recall, making it suitable for imbalanced class distributions. Class balancing is implemented using oversampling with SMOTE to improve classification performance.

## Results:🎯
The decision trees perform poorly compared to other models. The models struggle with predicting the leisure category and tend to predict a majority as current news.

Balancing the classes leads to improved results, especially in the leisure category. 

The best models are:

| Task | F1 | Leisure F1 |
| --- | --- | --- |
| SVC with Doc2Bow | 0.7655 | 0.52 |
| Logistic Regression with TF-IDF | 0.7741 | 0.45 |
| Linear SVC with LSA | 0.7589 | 0.38 |


Topic modeling using LSA and dense vector models like Doc2Bow further enhance the prediction accuracy. The LinearSVC model trained on LSA performs well, while Doc2Bow-based SVC shows good results, particularly in predicting the leisure class. 

A multilayer perceptron model using Keras does not achieve a satisfactory F1 score overall but performs better in classifying the leisure category. The Logistic Regression model with TF-IDF is selected as the best model due to its highest F1 score among the top models considered.

### [The Complete Article in Medium](https://guillemmiralles1.medium.com/news-classification-unbalanced-classes-nlp-e865ac33eb85)📜
