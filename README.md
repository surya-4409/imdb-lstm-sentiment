
# IMDB Sentiment Analysis using LSTM (PyTorch)

## Overview
This project implements a Long Short-Term Memory (LSTM) neural network using PyTorch to perform binary sentiment analysis on the IMDB movie reviews dataset. The goal is to classify reviews as positive or negative while building a complete, reproducible NLP pipeline.

## Dataset
- Source: IMDB Movie Reviews (50,000 reviews)
- Classes: Positive (1), Negative (0)
- Split: 70% Training, 15% Validation, 15% Test

## Model Architecture
- Embedding Layer (learned embeddings)
- Single-layer LSTM with 256 hidden units
- Dropout for regularization
- Fully connected output layer
- Loss Function: BCEWithLogitsLoss
- Optimizer: Adam

## Training
- Trained for 20 epochs
- Best model checkpoint saved based on validation accuracy
- GPU support enabled if available

## Results (Test Set)
- Accuracy: **85.17%**
- Precision: **84.37%**
- Recall: **86.35%**
- F1-score: **85.35%**

## Analysis
- Training and validation curves show stable convergence
- Error analysis highlights challenges with sarcasm and mixed sentiment
- t-SNE visualization confirms meaningful word embedding structure

## Repository Structure
```

imdb-lstm-sentiment/
├── data/
│   └── aclImdb/
├── notebooks/
│   └── imdb_lstm_sentiment.ipynb
├── models/
│   └── best_lstm_model.pth
├── outputs/
│   ├── loss_curve.png
│   ├── accuracy_curve.png
│   └── tsne_embeddings.png
├── requirements.txt
└── README.md

````

## Setup Instructions
```bash
pip install -r requirements.txt
````

Run the notebook from top to bottom:

```bash
jupyter notebook notebooks/imdb_lstm_sentiment.ipynb
```

## Notes

* The notebook is designed to run end-to-end without errors.
* All experiments are reproducible using the provided code and dataset structure.

## Video Demo

A short video walkthrough of the project, including model architecture, training, evaluation, and results, is available here:

🔗 Video Demo: https://drive.google.com/file/d/12INYSdxPKacrkE4SqAbtv0dT9uY4AfS3/view?usp=drive_link

## Author

**Name:** BILLAKURTI VENKATA SURYANARAYANA  
**Project:** IMDB Sentiment Analysis using LSTM (PyTorch)
