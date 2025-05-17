## Sentiment Analyzer – From TextBlob to Transformer-Based Models

### Project Overview

This project showcases a progressive sentiment analysis pipeline built in Python to evaluate customer feedback from a sample food blog dataset.

I began this work by implementing a lexicon-based model using `TextBlob`, which initially seemed sufficient for the task. However, through manual validation, I discovered the model lacked contextual accuracy. That insight led me to improve the approach by applying transformer-based models from HuggingFace—first a **2-class sentiment model**, and then a **3-class sentiment model** that can also classify **Neutral** sentiment.

This repository contains all three approaches and demonstrates how I validated and iterated to achieve higher accuracy in sentiment classification.

---

### Objectives

* Build an initial baseline using `TextBlob`
* Validate output quality through manual review of misclassified examples
* Improve sentiment classification using context-aware transformer models
* Showcase a product-like mindset in testing, evaluating, and refining the pipeline

---

### Tools & Technologies

* Python (executed in Google Colab)
* `TextBlob` for lexicon-based sentiment scoring
* HuggingFace `transformers` for contextual deep learning models
* `pandas` for data manipulation
* `cardiffnlp/twitter-roberta-base-sentiment` and `distilbert-base-uncased-finetuned-sst-2-english` models

---

### Files Included

| File                                    | Description                                                |
| --------------------------------------- | ---------------------------------------------------------- |
| `sample_food_feedback.csv`              | Input file containing 50 customer feedback entries         |
| `Sentiment Analyzer_TextBlob.ipynb`     | Notebook using `TextBlob` for rule-based sentiment scoring |
| `sample_food_feedback_with_sentiment.csv.csv` | Output file from TextBlob approach                         |
| `HuggingFace_Sentiment_Analysis_2ClassModel.ipynb`             | Notebook using HuggingFace 2-class sentiment model         |
| `feedback_with_2_class_sentiment.csv` | Output file from 2-class model                             |
| `HuggingFace_Sentiment_Analysis_2ClassModel.ipynb`             | Notebook using HuggingFace 3-class sentiment model         |
| `feedback_with_3_class_sentiment.csv` | Output file from 3-class model (includes NEUTRAL labels)   |

---

### Key Observations & Evolution

#### **Version 1: TextBlob (Lexicon-Based)**

* Labels based on polarity thresholds
* Easy to implement, but limited context awareness
* Misclassified mixed-tone or nuanced feedback
* Helpful for initial experimentation and understanding sentiment scoring

#### **Version 2: HuggingFace 2-Class Transformer**

* Used `distilbert-base-uncased-finetuned-sst-2-english`
* Great improvement in identifying positive vs. negative sentiment
* Accurately handled negation and contrast (e.g., “great food but slow service”)
* Lacked support for **neutral** classification

#### **Version 3: HuggingFace 3-Class Transformer**

* Used `cardiffnlp/twitter-roberta-base-sentiment`
* Added the ability to classify **Neutral** sentiment
* Delivered the most accurate results across all test cases
* Highly suitable for product feedback use cases with nuanced tone

---

### Reflections

This end-to-end exploration helped reinforce that:

* Lexicon-based models are useful as a starting point, but not production-ready for nuanced real-world feedback
* Context-aware transformer models significantly improve classification accuracy
* Adding support for **neutral sentiment** is critical in many product or customer-focused applications

---

### How to Run

1. Clone or download this repository
2. Choose any of the `.ipynb` notebooks (`TextBlob`, `2-Class`, or `3-Class`)
3. Open in **Google Colab** or **Jupyter Notebook**
4. Run all cells to load data, compute sentiment, and export results
5. Compare the outputs to observe performance differences
