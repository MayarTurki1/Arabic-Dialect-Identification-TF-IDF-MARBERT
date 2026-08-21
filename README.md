# Arabic Dialect Identification Using TF-IDF and MARBERT

A comparative NLP project for Arabic dialect classification, evaluating a traditional machine learning approach against a transformer-based language model.

---

## Overview

Arabic dialects vary significantly in vocabulary, spelling, and linguistic patterns, making automatic dialect identification a challenging Natural Language Processing task.

This project compares two approaches for Arabic dialect classification:

* **TF-IDF + Logistic Regression**
* **MARBERT**

The goal is to evaluate the difference between a traditional text classification pipeline and a transformer-based Arabic language model.

---

## Dataset

The dataset was obtained from **Kaggle** and contains approximately **112,000 Arabic text samples** representing multiple Arabic dialects.

The dataset was prepared and processed before training the classification models.

---

## Methodology

### 1. TF-IDF + Logistic Regression

A traditional machine learning pipeline was implemented using:

* Text preprocessing
* TF-IDF feature extraction
* Logistic Regression classification

TF-IDF was used to convert Arabic text into numerical feature representations before training the classifier.

---

### 2. MARBERT

A transformer-based approach was implemented using **MARBERT**, an Arabic language model designed for processing Arabic and dialectal text.

The model was fine-tuned for the Arabic dialect classification task.

The notebook also includes an interactive **Gradio interface** for testing the fine-tuned MARBERT model on Arabic text.

---

## Results

The two approaches were evaluated and compared using classification metrics.

| Model                        |   Accuracy |   Macro F1 |
| ---------------------------- | ---------: | ---------: |
| TF-IDF + Logistic Regression |            |            |
| MARBERT                      | **79.25%** | **67.51%** |

The results demonstrate the performance difference between the traditional TF-IDF-based approach and the transformer-based MARBERT model for Arabic dialect classification.

> Detailed evaluation results and visualizations are available in the project notebook.

---

## Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* Transformers
* Hugging Face
* MARBERT
* TF-IDF
* Logistic Regression
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
    ├───────────────┐
    ▼               ▼
TF-IDF           MARBERT
    │               │
    ▼               ▼
Logistic          Fine-Tuning
Regression           │
    │               │
    └───────┬───────┘
            ▼
    Dialect Classification
            │
            ▼
      Model Evaluation
```

---

## Interactive Demo

The project notebook includes a **Gradio interface** that allows users to enter Arabic text and test the fine-tuned MARBERT model for dialect prediction.

---

## Repository Contents

* `Arabic_Dialect_Identification_TF_IDF_MARBERT.ipynb` — Complete project workflow, model training, evaluation, and Gradio interface.
* `df_train.csv` — Dataset used in the project.

---

## Key Takeaway

This project provides a practical comparison between a traditional machine learning approach and a transformer-based model for Arabic dialect identification, highlighting the application of NLP techniques to Arabic and dialectal text.

---

## Project Type

**Individual Data Science / NLP Project**
