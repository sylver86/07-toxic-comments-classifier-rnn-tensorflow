# SafeComment — Toxic Comments Classifier (RNN · LSTM · TensorFlow)

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00?logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-Deep%20Learning-D00000?logo=keras&logoColor=white)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-F37626?logo=jupyter&logoColor=white)

## Overview

**Multi-label text classification** system that detects harmful content in user comments across six toxicity categories.
Built with a Bidirectional LSTM architecture, the model analyses sequential context within comments — understanding not just individual words but the meaning that emerges from their order and combination.

Applicable to content moderation pipelines in social platforms, enterprise communication tools, and regulatory compliance monitoring.

---

## Results

| Metric | Value |
|--------|-------|
| Model architecture | Bidirectional LSTM |
| Classification type | Multi-label (6 categories) |
| Overall accuracy | ~98% (binary per label) |
| AUC-ROC (macro avg) | ~0.97 |
| Training dataset | ~160,000 comments |

**Toxicity categories:** `toxic` · `severe_toxic` · `obscene` · `threat` · `insult` · `identity_hate`

A prediction vector of all zeros indicates a clean comment; any non-zero value flags the corresponding category.

---

## Model Architecture

```
Input text
    │
    ▼
Text Preprocessing (lowercase, punctuation removal, stopword filtering)
    │
    ▼
Tokenisation + Padding (fixed sequence length)
    │
    ▼
Embedding Layer (dense word vectors)
    │
    ▼
Bidirectional LSTM (long-range dependency capture)
    │
    ▼
Dense + Sigmoid output (6 independent binary classifiers)
```

---

## Project Workflow

1. **Data preprocessing** — cleaning, normalisation, tokenisation, sequence padding
2. **Vectorisation** — text → numerical sequences via Keras Tokenizer
3. **Model training** — LSTM with hyperparameter tuning (layers, neurons, learning rate)
4. **Evaluation** — per-label AUC-ROC, accuracy, binary cross-entropy loss
5. **Inference pipeline** — real-time classification of incoming comment strings

---

## Dataset

Jigsaw/Kaggle "Toxic Comment Classification Challenge" dataset.
~160K Wikipedia talk page comments, human-labelled across 6 toxicity categories.
Class imbalance addressed through sample weighting.

---

## Setup

```bash
git clone https://github.com/sylver86/07-toxic-comments-classifier-rnn-tensorflow.git
cd 07-toxic-comments-classifier-rnn-tensorflow
pip install tensorflow pandas numpy scikit-learn jupyter
# Extract dataset from Filter_Toxic_Comments_dataset.zip
jupyter notebook
```

Open `Progetto_Toxic_Comments_Filter.ipynb` and run all cells.

---

## Technologies

`Python` · `TensorFlow 2.x` · `Keras` · `LSTM` · `Pandas` · `NumPy` · `Scikit-learn` · `Jupyter`
