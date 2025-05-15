Sentiment Analyzer – HuggingFace 2-Class Transformer (Version 2)

Project Overview
 - This version builds upon the initial sentiment analysis work using TextBlob. After identifying limitations in the rule-based approach—particularly in understanding sentence context and mixed sentiments—I implemented a more context-aware solution using a HuggingFace transformer model.
 - This version uses the `distilbert-base-uncased-finetuned-sst-2-english` model to classify feedback, offering significantly improved performance on nuanced feedback.

Objectives
 - Replace lexicon-based scoring with a pretrained transformer model
 - Improve accuracy by using a context-aware deep learning approach
 - Validate how well the 2-class model performs on real-world user feedback
 - Compare results against the TextBlob baseline

Tools & Technologies
 - Python (in Google Colab)
 - HuggingFace Transformers library
 - Pretrained model: [`distilbert-base-uncased-finetuned-sst-2-english`](https://huggingface.co/distilbert-base-uncased-finetuned-sst-2-english)
 - `pandas` for data processing

Files Included
| File | Description |
|------|-------------|
| `HuggingFace_Sentiment_Analysis_2ClassModel.ipynb` | Notebook using HuggingFace 2-class transformer |
| `sample_food_feedback.csv` | Input file (same as version 1) |
| `feedback_with_2_class_sentiment.csv` | Output with POSITIVE or NEGATIVE labels and confidence scores |

Key Improvements Over Version 1
 - **Higher accuracy** for feedback with contrast or ambiguity (e.g., “great food but slow service”).
 - Better detection of clearly negative statements that TextBlob misclassified as positive.
 - Confidence score included to allow deeper insight into prediction certainty.

Reflection<br>
 - This model delivered significantly better results than the initial TextBlob approach. However, it does not offer a **"NEUTRAL"** classification, which may limit its utility for more nuanced or factual feedback.<br>
 - I developed **Version 3**, using a 3-class transformer model that includes **NEUTRAL** sentiment detection.

How to Run<br>
1. Open the `HuggingFace_Sentiment_Analysis_2ClassModel.ipynb` notebook in Google Colab.<br>
2. Upload the `sample_food_feedback.csv` or mount Google Drive.<br>
3. Run all cells to analyze and export sentiment-labeled feedback.

Related Versions<br>
 - [Version 1 - TextBlob](https://example.com)
 - [Version 1 – HuggingFace 3-Class Model Transformer] ()
