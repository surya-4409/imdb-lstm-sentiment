# End-to-End LSTM Sentiment Analysis on IMDb Reviews

## 📌 Project Links
* **GitHub Repository:** [surya-4409/imdb-lstm-sentiment](https://github.com/surya-4409/imdb-lstm-sentiment)
* **Video Demonstration:** [Watch the Project Demo](https://drive.google.com/file/d/1BaXRvIOgnMKmVsKggUXVOM-QOwpCze8V/view?usp=sharing)

---

## 📖 Project Overview
This project implements a Recurrent Neural Network (RNN) using PyTorch, specifically a **Long Short-Term Memory (LSTM)** network, to perform binary sentiment analysis on movie reviews. The objective is to build an automated Natural Language Processing (NLP) classifier capable of understanding sequential text data and accurately classifying reviews as positive or negative. 

The end-to-end deep learning workflow covers everything from raw text preprocessing and dynamic vocabulary generation to model training, evaluation, and semantic embedding visualization.

---

## 🛠️ Technical Stack
* **Programming Language:** Python
* **Deep Learning Framework:** PyTorch (including custom `Dataset` and `DataLoader`)
* **NLP & Data Processing:** NLTK, NumPy, Pandas
* **Data Visualization:** Matplotlib, Seaborn
* **Version Control:** Git, GitHub

---

## 📊 Dataset & Preprocessing
The model was trained and evaluated on the **IMDb Movie Reviews dataset**, consisting of 50,000 labeled reviews. The data pipeline includes the following robust preprocessing steps:
* **Text Cleaning:** Converted all raw text to lowercase, stripped special characters, and removed non-contributing stop words.
* **Tokenization & Vocabulary:** Tokenized the cleaned text and built a custom vocabulary strictly from the training data to prevent data leakage.
* **Sequence Mapping & Padding:** Converted text reviews into sequences of integer indices and padded them to a uniform length to enable efficient, multi-threaded batch processing.
* **Data Splitting:** Divided the dataset into training, validation, and test sets using a 70/15/15 ratio.

---

## 🧠 Model Architecture
The custom `torch.nn.Module` subclass consists of the following layers:
* **Embedding Layer (128 dimensions):** Learns dense vector representations of words, capturing semantic and contextual relationships between tokens.
* **LSTM Layer (256 hidden units):** A single-layer LSTM tracks sequential dependencies in the text data. A single layer was chosen to balance high performance with training stability.
* **Dropout (0.5 rate):** Applied to the LSTM output to heavily regularize the network and mitigate overfitting.
* **Fully Connected Layer:** A final linear layer with a Sigmoid activation function to output binary classification probabilities.

<<<<<<< HEAD
---
=======
## Setup Instructions
```bash
pip install -r requirements.txt
```
>>>>>>> 8d01fc4a5c58dd4a64c55a902933475a3e192e7e

## ⚙️ Training & Hyperparameters
The model was optimized through iterative experimentation and careful monitoring:
* **Loss Function:** `BCEWithLogitsLoss`
* **Optimizer:** Adam Optimizer 
* **Learning Rate:** 0.001 (provided fast, stable convergence)
* **Batch Size:** 64 (balanced memory efficiency and gradient stability)
* **Epochs:** 20 epochs with an early stopping checkpoint mechanism. The model weights with the best validation accuracy were saved to prevent overfitting.

---

## 🏆 Achievements & Evaluation
The model successfully exceeded the primary project benchmark of 80% accuracy, demonstrating strong generalization to unseen text.

* **Final Test Accuracy:** **85.17%**
* **Training Stability:** Loss and accuracy curves demonstrate smooth, consistent convergence over the training lifecycle.
* **Semantic Learning (t-SNE):** t-SNE visualizations confirm the embedding layer successfully learned meaningful word representations by clustering semantically related words together.
* **Qualitative Error Analysis:** Misclassified samples were manually analyzed, revealing that the model's primary failure modes involve highly nuanced language, such as heavy sarcasm, mixed sentiment, or long reviews with shifting emotional polarity.

---

## 📁 Repository Structure
* `notebooks/imdb_lstm_sentiment.ipynb`: The primary Jupyter Notebook containing the complete end-to-end code[cite: 2].
* `models/best_lstm_model.pth`: The saved PyTorch weights of the highest-performing model[cite: 2].
* `outputs/`: Directory containing all evaluation graphics, including `accuracy_curve.png`, `loss_curve.png`, and `tsne_embeddings.png`[cite: 2].
* `requirements.txt`: Environment dependencies required to run the project[cite: 2].
* `README.md`: Project documentation[cite: 2].