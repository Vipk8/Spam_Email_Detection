# Spam Email Detection System
![image](https://github.com/user-attachments/assets/c92d64fc-8a9f-40ab-b1db-3c0ecd20566a)


## Overview

Spam email detection is a crucial feature for enhancing user experience and security by automatically identifying and filtering out unwanted emails. This project focuses on building a robust spam detection system using **Natural Language Processing (NLP)** and **machine learning techniques** to classify emails as spam or ham (non-spam).

## Project Structure

The project is organized into the following components:
1. Data: A labeled dataset of emails (spam or ham) used for training and testing.
2. Preprocessing: Steps to clean and prepare the email data for model training.
3. Modeling: Training machine learning models to classify emails.
4. Evaluation: Measuring the model's performance using various metrics.
5. Pipeline: An end-to-end workflow from data preprocessing to prediction.
6. Testing: Demonstrating the model's performance on unseen email samples.

## Data Description

The dataset consists of:
- Category: Specifies whether an email is `spam` or `ham`.
- Message: The actual content of the email.

The data is loaded from a CSV file, explored for patterns, and prepared for processing and modeling.

## Data Preprocessing

Preprocessing is essential for preparing raw text data for machine learning. Key steps include:

1. Lowercasing: Converts all text to lowercase for uniformity.
2. Removing Punctuation: Eliminates unnecessary punctuation marks.
3. Removing Non-Alphabetic Characters: Filters out numbers and special characters.
4. Tokenization: Splits email messages into individual words for analysis.
5. Removing Stop Words: Discards common words like "and," "the," and "is" that add little value to classification.
6. Lemmatization: Reduces words to their root forms (e.g., "running" becomes "run").

These steps ensure the text data is clean, consistent, and ready for vectorization.

## Machine Learning Modeling

This project employs the **Extra Trees Classifier**, a robust ensemble learning algorithm, to classify emails. The key modeling steps are:

1. Vectorization: Converts the cleaned text into numerical format using **TF-IDF (Term Frequency-Inverse Document Frequency)**.
2. Training: Fits the model on the processed data.
3. Oversampling: Balances the dataset by increasing the representation of the minority class (spam emails).

## Model Evaluation

The model's performance is assessed using the following metrics:
- Accuracy: Overall correctness of the model.
- Precision: Proportion of correctly identified spam emails.
- Recall: Proportion of actual spam emails correctly identified.
- F1-Score: Harmonic mean of precision and recall.

A confusion matrix is used to visualize the classification results, illustrating the model's ability to distinguish between spam and ham.

## End-to-End Pipeline

An automated pipeline is created to handle the full workflow:
1. Data preprocessing
2. Feature vectorization
3. Model training and prediction

This pipeline can be easily deployed for real-time spam detection in email systems.

## Testing and Results

The system's performance is demonstrated using example emails:
- Example 1:  
  Message: Congratulations! You've won a $1000 Walmart gift card. Click here to claim your prize now!
  Prediction: Spam  

- Example 2:  
  Message: Don't forget our meeting at 3 PM today. Looking forward to discussing the new project.
  Prediction: Ham  

The model shows reliable and consistent performance, effectively distinguishing spam from legitimate emails.

## Conclusion
This project successfully implements a spam detection system using NLP and machine learning. The system is accurate, efficient, and can be seamlessly integrated into email services to improve security and user satisfaction.

## Requirements
To run this project, you will need the following Python libraries:

- pandas
- matplotlib
- seaborn
- scikit-learn
- imblearn
- nltk
