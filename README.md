# Arabic Dialect Identification Using TF-IDF and MARBERT

A comparative NLP project for Arabic dialect identification using a traditional machine learning approach with TF-IDF and Logistic Regression, and a transformer-based deep learning approach using MARBERT.

## Project Overview

This project focuses on identifying Arabic dialects from text using two different approaches:

- Logistic Regression with TF-IDF
- MARBERT transformer model

The project compares the performance of traditional machine learning and transformer-based deep learning for multi-class Arabic dialect classification.

The dataset contains 112,000 Arabic text samples from multiple Arabic-speaking countries and dialect classes.

## Objectives

- Identify the dialect of an Arabic text sample.
- Compare a traditional machine learning approach with a transformer-based approach.
- Evaluate model performance using Accuracy and Macro F1-score.
- Test the models on new Arabic text samples.
- Develop an interactive interface for dialect prediction using MARBERT.

## Dataset

The dataset was obtained from the MADAR corpus and contains Arabic text samples associated with different countries and dialects.

The dataset contains 112,000 records and 7 columns, including:

- `lang`
- `sent`
- `city`
- `country_id`
- `country`
- `city_id`
- `source`

The `sent` column contains the Arabic text, while the `country` column is used as the target label for dialect classification.

## Arabic Text Preprocessing

The text preprocessing pipeline includes:

- Removing Arabic diacritics
- Normalizing Arabic characters
- Removing non-Arabic characters
- Reducing repeated characters
- Normalizing whitespace
- Removing rows with missing text or labels

The processed text is then used for model training and evaluation.

## Methodology

The project follows the following workflow:

**Data Loading → Data Exploration → Text Preprocessing → Label Encoding → Train/Test Split → Model Training → Evaluation → Model Comparison**

### 1. Logistic Regression with TF-IDF

The traditional machine learning approach uses:

- TF-IDF Vectorization
- Unigrams and bigrams
- Maximum of 50,000 features
- Minimum document frequency of 3
- Logistic Regression with balanced class weights

The dataset is split into 85% training data and 15% testing data.

### 2. MARBERT

The deep learning approach uses the pretrained:

`UBC-NLP/MARBERT`

The model is fine-tuned for multi-class Arabic dialect classification.

Training configuration includes:

- Learning rate: 1e-5
- Training batch size: 16
- Evaluation batch size: 32
- Maximum sequence length: 128
- Epochs: 2
- Weight decay: 0.02
- AdamW optimizer
- Early stopping

## Results

The two approaches achieved the following results:

| Model | Accuracy | F1 Macro |
|---|---:|---:|
| Logistic Regression (TF-IDF) | 72.43% | 60.91% |
| **MARBERT** | **79.25%** | **67.51%** |

### Key Finding

MARBERT achieved better performance than Logistic Regression with TF-IDF on the evaluated dataset.

The results show an improvement in both Accuracy and Macro F1-score when using the transformer-based approach.

## Model Testing

The Logistic Regression model was tested on new Arabic sentences to demonstrate dialect prediction.

Example inputs included Arabic sentences representing different dialects, such as:

- `وين اقرب مطعم كشري؟`
- `وش الأخبار عندكم اليوم`
- `شنو أحسن قهوة في الدوحة؟`

## Interactive Interface

A Gradio interface was developed using the fine-tuned MARBERT model.

The interface allows users to enter an Arabic sentence and receive:

- Predicted dialect
- Prediction confidence

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- MARBERT
- TF-IDF
- Logistic Regression
- Matplotlib
- Seaborn
- Gradio
- Google Colab

## Repository Contents

- `Project_NLP_Arabic_Dialect_Identification_Using_Machine_Learning_and_MARBERT (1).ipynb` — Project implementation, preprocessing, model training, evaluation, and comparison
- `df_train.csv` — Dataset

## Models Comparison

The project demonstrates the difference between:

**Traditional Machine Learning**

TF-IDF → Logistic Regression

and

**Transformer-based Deep Learning**

MARBERT → Fine-tuning → Dialect Classification
