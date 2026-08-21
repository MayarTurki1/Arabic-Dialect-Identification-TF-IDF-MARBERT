# Arabic Dialect Identification Using TF-IDF and MARBERT

A comparative NLP project for Arabic dialect classification, evaluating a traditional machine learning approach against a transformer-based language model.

---

## Overview

Arabic dialects vary significantly in vocabulary, spelling, and linguistic patterns, making automatic dialect identification a challenging Natural Language Processing task.

This project compares two approaches for Arabic dialect classification:

* **TF-IDF + Logistic Regression**
* **MARBERT**

The objective is to evaluate the performance difference between a traditional text classification pipeline and a transformer-based Arabic language model.

---

## Dataset

The dataset was obtained from **Kaggle** and contains approximately **112,000 Arabic text samples** representing multiple Arabic dialects.

The data was cleaned and preprocessed before training the classification models.

---

## Methodology

### 1. TF-IDF + Logistic Regression

A traditional machine learning pipeline was implemented using:

* Arabic text preprocessing
* TF-IDF feature extraction
* Logistic Regression classification

The TF-IDF vectorizer was configured with unigram and bigram features before training the classifier.

---

### 2. MARBERT

A transformer-based approach was implemented using **MARBERT**, an Arabic language model designed to handle Arabic and dialectal text.

The model was fine-tuned for the Arabic dialect classification task using the Hugging Face Transformers framework.

The training configuration included:

* Learning rate: `1e-5`
* Training epochs: `2`
* Training batch size: `16`
* Evaluation batch size: `32`
* Maximum sequence length: `128`
* Weight decay: `0.02`

---

## Results

Both models were evaluated using **Accuracy** and **Macro F1**.

| Model                        |   Accuracy |   Macro F1 | Training Approach               |
| ---------------------------- | ---------: | ---------: | ------------------------------- |
| Logistic Regression + TF-IDF | **72.43%** | **60.91%** | Traditional Machine Learning    |
| MARBERT                      | **79.25%** | **67.51%** | Transformer-based Deep Learning |

### Performance Comparison

MARBERT achieved higher performance than the TF-IDF + Logistic Regression baseline on both evaluation metrics:

* **+6.82 percentage points** in Accuracy
* **+6.60 percentage points** in Macro F1

This demonstrates the advantage of the transformer-based approach for the dialect classification task evaluated in this project.

---

## Interactive Demo

The project notebook includes an interactive **Gradio interface** for testing the fine-tuned MARBERT model.

Users can enter an Arabic sentence and receive:

* Predicted dialect
* Prediction confidence

The interface supports classification across the dialect labels included in the trained model.

---

## Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* Hugging Face Transformers
* MARBERT
* TF-IDF
* Logistic Regression
* PyTorch
* NLP
* Gradio
* Jupyter Notebook

---

## Project Workflow

```text
Arabic Text
     │
     ▼
Text Preprocessing
     │
     ├──────────────────┐
     ▼                  ▼
  TF-IDF             MARBERT
     │                  │
     ▼                  ▼
Logistic             Fine-Tuning
Regression               │
     │                  │
     └────────┬─────────┘
              ▼
      Dialect Classification
              │
              ▼
        Model Evaluation
              │
              ▼
       Performance Comparison
```

---

## Repository Contents

* `Project_NLP_Arabic_Dialect_Identification_Using_Machine_Learning_and_MARBERT.ipynb` — Complete project workflow, preprocessing, model training, evaluation, comparison, and Gradio interface.
* `df_train.csv` — Dataset used in the project.

---

## Key Takeaway

This project provides a practical comparison between traditional machine learning and transformer-based deep learning for Arabic dialect identification.

The results show that **MARBERT outperformed the TF-IDF + Logistic Regression baseline** in both Accuracy and Macro F1 on the evaluated dataset.
