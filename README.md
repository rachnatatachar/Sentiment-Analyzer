# Sentiment-Analyzer

__Project Overview__<br>
This project is the first version of a sentiment analysis tool built in Python using the TextBlob library. The goal is to evaluate and categorize customer feedback as Positive, Neutral, or Negative based on sentiment polarity. <br>
This notebook is part of a series where I explore and compare sentiment analysis approaches, starting with lexicon-based methods and moving toward more context-aware machine learning models.

__Objectives__<br>
 - Evaluate sentiment in customer feedback using TextBlob, a lexicon-based sentiment analysis tool
 - Assign sentiment labels based on polarity thresholds
 - Analyze the accuracy of the results through manual validation
 - Use this baseline to inform the next iteration of model selection and approach

__Tools & Technologies__<br>
 - Python (executed in the Jupyter)
 - `TextBlob` for sentiment scoring
 - `pandas` for data processing
 - Sample CSV dataset with 50 feedback entries from a food blog scenario

__Files Included__<br>
| File                                   | Description                                                   |
| -------------------------------------- | ------------------------------------------------------------- |
| `sentiment_textblob.ipynb`             | Jupyter notebook using `TextBlob` to score and label feedback |
| `sample_food_feedback.csv`             | Input file containing raw feedback entries                    |
| `feedback_with_textblob_sentiment.csv` | Output with added polarity score and sentiment label per row  |

__Key Observations__<br>
 - This approach provided a working sentiment classifier with polarity and subjectivity scores.
 - However, accuracy was noticeably off in several cases:
   - Mixed-tone reviews (e.g., “okay but slow”) were labeled as Positive
   - Sentences like “too sweet for my taste” were also tagged Positive, likely due to word-level interpretation
 - Contextual understanding was limited, as expected from a rule-based model

__Reflection__<br>
 - Although TextBlob is a well-known method, it lacks the nuance required for high-accuracy sentiment classification in real-world feedback.
 - It also provided a strong foundation for evaluating better-performing models based on contextual embeddings and supervised learning.

__What's Coming Next?__ <br>
To improve sentiment classification:
 - I have explored HuggingFace 2-class transformer model to assess contextual performance.
 - This next version is built directly upon the learnings from this one.

__How to Run__<br>
 - Download this repository
 - Open `sentiment_textblob.ipynb` in Google Colab or Jupyter
 - Run all cells to load data, process sentiment, and export results
