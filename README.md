# 🧠 Sentiment Analysis using RNN
## 📌 Overview

This project implements a Sentiment Analysis model using a Recurrent Neural Network (RNN) to classify text into positive or negative sentiment.

The goal was not just to build a working model, but to understand sequence modeling, limitations of vanilla RNNs, and explore how performance can be improved using more advanced architectures.

## 🚀 Key Highlights
- Built a Simple RNN-based NLP pipeline from raw text
- Implemented text preprocessing + tokenization
- Designed and trained a sequence model using Keras
- Analyzed model limitations (vanishing gradients, context loss)
- Explored improvements using:
  - LSTM
  - Bidirectional LSTM (BiLSTM)
## 🧱 Project Pipeline
1. Data Preprocessing
- Lowercasing text
- Removing punctuation, URLs, and noise
- Tokenization using Keras Tokenizer
- Padding sequences for fixed-length input
2. Feature Engineering
- Vocabulary creation
- Integer encoding of words
- Sequence padding
3. Model Architecture
  ```
  Embedding → SimpleRNN → Dense → Output
  ```
- *Embedding Layer:* Converts words into dense vectors
- *SimpleRNN Layer:* Captures sequential dependencies
- *Dense Layer:* Final classification
## 🧪 Model Configuration
- Loss Function: `sparse_categorical_crossentropy`
- Optimizer: `Adam`
- Evaluation Metric: `Accuracy`
## 📊 Results
- Achieved baseline accuracy using Simple RNN
- Observed:
  - Difficulty in capturing long-term dependencies
  - Performance degradation on longer sequences
## ⚠️ Limitations (Yes, I Know Them)
This is where most people lie. I won’t.
- Vanilla RNN suffers from vanishing gradients
- Weak performance on long sequences
- Limited context retention
## 🔧 Improvements Explored
- LSTM (Long Short-Term Memory)
  - Handles long-term dependencies better
  - Introduces memory cell and gating mechanisms
- Bidirectional LSTM
  - Processes sequence forward + backward
  - Improves context understanding
Example upgraded architecture:
```
Embedding → Bidirectional(LSTM) → Dense → Output
```
## 📈 Future Enhancements
- Use pre-trained embeddings (GloVe / Word2Vec)
- Hyperparameter tuning (embedding size, sequence length)
- Add Dropout to reduce overfitting
- Try GRU / Transformer-based models
- Use attention mechanisms
## 🛠️ Tech Stack
- Python
- TensorFlow / Keras
- NumPy
- Pandas
## 💡 What This Project Demonstrates
This project shows that I:
- Understand sequence modeling fundamentals
- Can build an end-to-end NLP pipeline
- Know the limitations of Simple RNNs
- Can critically evaluate and improve models
## 💡 Key Learnings
- RNNs are simple but not scalable for complex NLP tasks
- Data preprocessing impacts performance more than model tweaks
- Sequence length and padding strategy matter significantly
## 👨‍💻 Author
**Subhajit Mandal**  
Machine Learning Enthusiast  
📧 Email: rana587mandal@gmail.com  
🔗 LinkedIn: www.linkedin.com/in/subhajit-mandal-047649273
