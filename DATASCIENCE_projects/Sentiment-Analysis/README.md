# 💬 Social Media Sentiment Analysis

A mini project to analyze sentiment in social media posts using Natural Language Processing. The goal is to classify posts as **Positive**, **Neutral**, or **Negative**, and understand trends through visualization.

---

## 📁 Dataset

The dataset includes:
- Social media messages (tweets/posts)
- Labeled sentiment for training data
- No labels for validation/test data

---

## 🔧 Steps Involved

### 1. 🧹 Data Cleaning
- Removed URLs, mentions, hashtags, special characters
- Converted text to lowercase
- Removed stopwords
- Tokenized and lemmatized the text

### 2. 🧪 Preprocessing
- Extracted message length
- Created a new column for sentiment labels (for classification)
- Prepared datasets for training and validation

---

## 📊 Visualizations

### 📍 1. Sentiment Distribution
Shows the number of positive, neutral, and negative messages in:
- **Training Data**
- **Validation Data**


### 📍 2. Entity Distribution (Training Data)
Visualizes how many messages contain certain keywords/entities, such as:

- **Brands**
- **Topics**
- **Hashtags**

### 🧠 Tools Used
**Pandas & NumPy for data handling**
**NLTK for text processing**
**Seaborn & Matplotlib for visualization**


