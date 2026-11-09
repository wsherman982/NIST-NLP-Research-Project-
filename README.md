# NIST Cybersecurity Framework NLP Classification

## Project Overview

This research project uses Natural Language Processing (NLP)
to classify cybersecurity statements from the NIST
Cybersecurity Framework (CSF) 2.0.

The project focuses on three cybersecurity functions:
- Govern
- Identify
- Protect

## Dataset

74 NIST CSF 2.0 statements:
- Govern: 31
- Identify: 21
- Protect: 22

Training dataset: 55 statements
Testing dataset: 19 statements

## Machine Learning Models

1. TF-IDF + Logistic Regression
2. TF-IDF + Multinomial Naive Bayes
3. DistilBERT

## Preliminary Results

Held-out test results:

| Model | Accuracy | Macro F1 |
|---|---:|---:|
| Majority Baseline | 42.11% | 0.198 |
| Logistic Regression | 84.21% | 0.834 |
| DistilBERT | 63.16% | 0.604 |

Five-fold cross-validation results:

| Model | Mean Accuracy | Mean Macro F1 |
|---|---:|---:|
| Logistic Regression | 75.7% | 0.731 |
| Multinomial Naive Bayes | 73.0% | 0.698 |

## Key Findings

Logistic Regression outperformed DistilBERT on the
19-statement held-out test set.

The small dataset may have limited DistilBERT's
fine-tuning performance.

Further evaluation is needed before generalizing
these findings.

## Technologies

Python, Jupyter Notebook, pandas, scikit-learn,
PyTorch, Hugging Face Transformers, and PyMuPDF.

## Data Source

NIST Cybersecurity Framework (CSF) 2.0

https://doi.org/10.6028/NIST.CSWP.29
