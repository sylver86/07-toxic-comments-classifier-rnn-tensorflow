# SafeComment — Classificatore di Commenti Tossici con Deep Learning

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00?logo=tensorflow&logoColor=white)
![LSTM](https://img.shields.io/badge/Model-Bidirectional%20LSTM-purple)
![AUC-ROC](https://img.shields.io/badge/AUC--ROC-~0.97-brightgreen)

## Panoramica

Classificatore multi-label per la rilevazione automatica di commenti tossici su 6 categorie (toxic, severe_toxic, obscene, threat, insult, identity_hate) con Bidirectional LSTM su TensorFlow/Keras. Addestrato su 160.000 commenti reali (Kaggle), raggiunge AUC-ROC ~0.97 e accuracy ~98%.

Architettura Deep Learning per NLP applicabile a piattaforme di content governance, AI safety, compliance communication e sistemi di moderazione contenuti in ambito enterprise.

## Valore Enterprise

| Settore / Azienda | Rilevanza |
|-------------------|-----------|
| Difesa & Sicurezza (Leonardo) | AI safety, analisi comunicazioni anomale, sistemi di allerta |
| IT Consulting (NTT Data, Accenture) | Deep Learning NLP per governance contenuti digitali |
| Media & Telco | Moderazione contenuti generati da utenti (UGC) |
| Banking & Insurance | Analisi tossicità comunicazioni, compliance monitoring |

## Risultati

| Metrica | Valore |
|---------|--------|
| AUC-ROC | ~0.97 |
| Accuracy | ~98% |
| Training samples | 160.000 commenti reali |
| Categorie classificate | 6 (multi-label) |
| Architettura | Bidirectional LSTM |

## Architettura del Modello

```
Input testuale
      │
      ▼
Tokenizzazione + Padding (Keras Tokenizer)
      │
      ▼
Embedding Layer (vettori appresi end-to-end)
      │
      ▼
Bidirectional LSTM
(cattura contesto in entrambe le direzioni)
      │
      ▼
Dense Layer + Sigmoid (×6 output)
      │
      ▼
6 label indipendenti: toxic · severe_toxic · obscene
                      threat · insult · identity_hate
```

## Setup

```bash
git clone https://github.com/sylver86/07-toxic-comments-classifier-rnn-tensorflow.git
cd 07-toxic-comments-classifier-rnn-tensorflow
pip install -r requirements.txt
jupyter notebook notebooks/Progetto_Toxic_Comments_Filter.ipynb
```

## Struttura Repository

```
07-toxic-comments-classifier-rnn-tensorflow/
├── notebooks/
│   └── Progetto_Toxic_Comments_Filter.ipynb
├── data/
│   └── Filter_Toxic_Comments_dataset.zip
├── requirements.txt
└── README.md
```

## Stack Tecnologico

`Python 3.8+` · `TensorFlow 2.x` · `Keras` · `Bidirectional LSTM` · `pandas` · `NumPy` · `scikit-learn`

---

---

# SafeComment — Toxic Comments Classifier with Deep Learning 🇬🇧

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00?logo=tensorflow&logoColor=white)
![AUC-ROC](https://img.shields.io/badge/AUC--ROC-~0.97-brightgreen)

## Overview

Multi-label classifier for automatic detection of toxic comments across 6 categories (toxic, severe_toxic, obscene, threat, insult, identity_hate) using a Bidirectional LSTM on TensorFlow/Keras. Trained on 160,000 real comments (Kaggle), achieves AUC-ROC ~0.97 and ~98% accuracy.

## Results

| Metric | Value |
|--------|-------|
| AUC-ROC | ~0.97 |
| Accuracy | ~98% |
| Training samples | 160,000 real comments |
| Output labels | 6 (multi-label) |
| Architecture | Bidirectional LSTM |

## Model Architecture

```
Text input  →  Tokenizer + Padding  →  Embedding Layer
    →  Bidirectional LSTM  →  Dense + Sigmoid (×6)
    →  6 independent labels
```

## Setup

```bash
git clone https://github.com/sylver86/07-toxic-comments-classifier-rnn-tensorflow.git
cd 07-toxic-comments-classifier-rnn-tensorflow
pip install -r requirements.txt
jupyter notebook notebooks/Progetto_Toxic_Comments_Filter.ipynb
```

## Technologies

`Python 3.8+` · `TensorFlow 2.x` · `Keras` · `Bidirectional LSTM` · `pandas` · `NumPy` · `scikit-learn`
