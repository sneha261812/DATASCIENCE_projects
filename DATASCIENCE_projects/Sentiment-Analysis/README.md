# Prodigy-Infotech-Internship-Task-4

# 💬 Social Media Sentiment Analysis

Analyze and visualize sentiment trends in social media content to gain actionable insights into **public opinion**, **brand perception**, or **topic engagement**.

---

## 🧭 Project Objective

This project focuses on using Natural Language Processing (NLP) techniques to classify social media posts (e.g., tweets) into sentiment categories such as:

- ✅ **Positive**
- ⚪ **Neutral**
- ❌ **Negative**

Visualizations such as word clouds and time-based sentiment trends provide a deeper understanding of emotional tone and user engagement over time.

---

## 📦 Tools & Technologies

| Library        | Purpose                                 |
|----------------|------------------------------------------|
| `Pandas`       | Data loading and manipulation            |
| `NLTK`, `TextBlob`, `VADER` | Text preprocessing & sentiment classification |
| `Matplotlib`, `Seaborn` | Data visualization                 |
| `WordCloud`    | Visualizing frequent keywords            |
| `re` (Regex)   | Text cleaning                            |

---

## 📁 Data Source

- **Option 1:** Real-time data from the **Twitter API** using Tweepy  
- **Option 2:** Pre-collected **CSV dataset** of tweets or posts with timestamp and content

---

## 🧹 Data Cleaning & Preprocessing

### 1️⃣ Text Cleaning
- Remove URLs, hashtags, mentions
- Convert to lowercase
- Remove special characters and numbers
- Eliminate stopwords (using NLTK)
- Tokenize and lemmatize text

```python
import re
from nltk.corpus import stopwords

def clean_text(text):
    text = re.sub(r"http\S+|www\S+|https\S+", '', text)
    text = re.sub(r'\@\w+|\#','', text)
    text = re.sub(r'[^A-Za-z\s]', '', text)
    text = text.lower()
    return ' '.join([word for word in text.split() if word not in stopwords.words('english')])
