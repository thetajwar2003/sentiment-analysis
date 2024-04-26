# Twitter Sentiment Analysis Project

## Project Overview
This project focuses on performing sentiment analysis on tweets. It involves various preprocessing techniques to clean and prepare the data, followed by the application of both traditional machine learning models and deep learning approaches to classify sentiments.

## Data Source
The dataset used for this project can be found on Kaggle: [Sentiment140 dataset by Stanford](https://www.kaggle.com/datasets/kazanova/sentiment140).

## Preprocessing Steps
The preprocessing pipeline includes:
- **Lowercasing**: Convert all text to lowercase to maintain uniformity.
- **Removing stopwords**: Eliminate common words such as 'the' and 'a' that do not contribute to sentiment analysis.
- **Removing links, usernames, and hashtags**: Clean tweets by removing unnecessary metadata.
- **Replacing emojis**: Translate emojis to text to capture their sentiment.
- **Removing unknown words and special characters**: Ensure the data contains only known and relevant words.
- **Changing words with repeated characters**: Standardize words like 'cooool' to 'cool'.
- **Lemmatization**: Reduce words to their base or dictionary form.

## Feature Engineering
- **TF-IDF (Term Frequency-Inverse Document Frequency)**: Convert text data into a matrix of TF-IDF features.
- **Bag of Words**: Transform text into a sparse matrix of word counts.
- **Word Embeddings (GloVe)**: Use pre-trained GloVe embeddings as features for deep learning models.

## Machine Learning Models
Each model is integrated into a pipeline that includes the appropriate feature transformation (TF-IDF or Bag of Words).
- **Linear SVM (Support Vector Machine)**
- **Multinomial Naive Bayes**
- **Decision Trees**
- **Logistic Regression**

## Deep Learning Models
These models utilize GloVe embeddings to capture more complex patterns in the data.
- **Simple Neural Network**
- **Convolutional Neural Network (CNN)**


## Results

### Machine Learning Models

| Model                   | Accuracy | Precision (Negative) | Precision (Positive) | Recall (Negative) | Recall (Positive) | F1-Score (Negative) | F1-Score (Positive) |
|-------------------------|---------:|---------------------:|---------------------:|------------------:|------------------:|--------------------:|--------------------:|
| SVM Classifier          |     81%  |                 82%  |                 81%  |               80% |               82% |                 81% |                 81% |
| Multinomial Naive Bayes |     80%  |                 79%  |                 80%  |               81% |               79% |                 80% |                 79% |
| Decision Tree Classifier|     61%  |                 60%  |                 63%  |               68% |               55% |                 64% |                 59% |
| Logistic Regression     |     82%  |                 83%  |                 82%  |               81% |               83% |                 82% |                 83% |


### Deep Learning Models

| Model                | Best Validation Accuracy | Best Validation Loss |
|----------------------|-------------------------:|---------------------:|
| Simple Neural Network|                    73.58%|                0.5463|
| CNN                  |                    84.99%|                0.4409|

