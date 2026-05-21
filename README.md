# Sentiment Analysis of Iraqi Telecom App Reviews

This repository contains the SWE530 Advanced Natural Language Processing course project:

**Sentiment Analysis of Iraqi Telecom App Reviews Using TF-IDF, SVM, and Arabic Transformer Models**

## Project Overview

This project investigates binary sentiment classification for Iraqi Arabic telecom application reviews. It compares a classical machine learning pipeline based on **TF-IDF + SVM** with an Arabic transformer-based approach using **CAMeLBERT**.

## Repository Structure

```text
notebooks/
  Sentiment_Analysis_of_Iraqi_Telecom_App_Reviews.ipynb

data/
  raw/
    iraqi_telecom_reviews_raw.csv
  processed/
    iraqi_telecom_reviews_clean.csv
    X_test_fair.csv
    y_test_fair.csv
    models_evaluation_results.csv

models/
  svm_model.pkl
  tfidf_vectorizer.pkl

presentation/
  SWE530_NLP_SentimentAnalysis_v2.pptx

report/
  Colab_Notebook_Report.pdf
```

## Dataset

The dataset contains Iraqi telecom mobile app reviews collected from Google Play. The reviews are labeled as binary sentiment classes:

- `1` = Positive
- `0` = Negative

The raw dataset is cleaned and normalized to handle noisy Arabic text, dialectal spelling, short reviews, and mixed Arabic-English content.

## Methods

### Text Preprocessing

- URL and noise removal
- Arabic character normalization
- Diacritic and elongation removal
- Extra whitespace cleanup
- Preservation of Iraqi dialect-specific vocabulary

### Classical Machine Learning

- TF-IDF vectorization
- Linear Support Vector Machine classifier
- Evaluation using accuracy, macro precision, macro recall, macro F1-score, and ROC-AUC

### Arabic Transformer Model

- CAMeLBERT-based Arabic sentiment analysis
- Evaluation on the same fair test split used for the SVM model

## Main Result

The classical **SVM + TF-IDF** baseline achieved the strongest overall result in this project, showing that classical NLP methods can perform very well on short, noisy, dialectal Arabic reviews.

## Course Information

- Course: SWE530 – Advanced Natural Language Processing
- Instructor: Dr. Beyza Eken
- Program: Software Engineering Master's Program
- Student: Mohammed Radhi Khamees

## Notes

Do not commit API keys, tokens, or private credentials inside notebooks.
