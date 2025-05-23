#  Binary Sentiment Classification of Movie Reviews

##  Objective
The objective of this project is to develop a binary classifier that can predict the sentiment (positive or negative) of a movie review. The target metric is an **accuracy of at least 0.85** on the test set.

---

##  Exploratory Data Analysis (EDA)

- Dataset: 50,000 movie reviews (balanced: 25,000 positive, 25,000 negative).
- No missing values, balanced classes.
- Review lengths vary significantly, with a wide vocabulary range.

**Conclusion:** The dataset is clean and balanced, making it suitable for binary classification tasks.

---

##  Text Preprocessing

Steps taken:
- Converted text to lowercase
- Removed HTML tags, punctuation, and numbers
- Stop-word removal using NLTK
- Compared **stemming** (PorterStemmer) and **lemmatization** (WordNetLemmatizer)

**Conclusion:** Lemmatization was chosen for its better generalization and readability.

---

##  Feature Engineering

- Vectorization technique: **TF-IDF** with max 10,000 features
- Compared with CountVectorizer: TF-IDF provided better accuracy

**Conclusion:** TF-IDF was selected for model training.

---

##  Model Evaluation

Three models were tested on the test set (8,000 reviews):

| Model                | Accuracy | Precision | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| Naive Bayes          | 0.8570   | 0.86      | 0.85   | 0.86     |
| Logistic Regression  | **0.8858** | 0.89    | 0.89   | 0.89     |
| Linear SVC           | 0.8798   | 0.88      | 0.88   | 0.88     |

### Detailed Classification Reports

#### Naive Bayes:
- **Accuracy:** 0.8570
- F1-score: 0.86 for both classes
- Good baseline model, fast and efficient

#### Logistic Regression:
- **Accuracy:** 0.8858
- Best F1-score: 0.88–0.89
- Excellent performance and interpretability

#### Linear SVC:
- **Accuracy:** 0.8798
- F1-score: 0.88
- Strong performance, slightly behind Logistic Regression

---

##  Final Model Selection

- **Selected Model:** Logistic Regression
- **Justification:**
  - Highest accuracy (0.8858)
  - Balanced precision, recall, and F1-score
  - Robust, interpretable, and efficient for deployment

---

##  Overall Performance

- Final accuracy: **0.8858**
- All models surpassed the target accuracy of 0.85
- Model generalizes well with no overfitting signs

---

##  Business Value

### Applications:
- Automate customer sentiment analysis for movie or product reviews
- Enhance decision-making for marketing strategies
- Power recommendation systems and feedback analysis tools

### Value:
- Reduces manual review workload
- Provides real-time sentiment insight
- Enhances user engagement and satisfaction

---

##  Conclusion

The Logistic Regression-based sentiment classifier meets the target accuracy and demonstrates robust, balanced performance. It is ready for deployment in various NLP-driven sentiment analysis applications.

