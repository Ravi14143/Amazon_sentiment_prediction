---

# Amazon Product Review Sentiment Analysis

This Streamlit web application allows users to predict the sentiment of Amazon product reviews. Users can either select a product ID to view its reviews and overall sentiment or input a custom review text to get sentiment analysis. Positive and negative keywords contributing to the sentiment are also highlighted.

---

## Features

* View reviews for a selected product ID.
* Display overall sentiment of a product based on reviews.
* Highlight positive and negative words contributing to the sentiment.
* Predict sentiment for a custom review input.
* Recommend whether a product is worth buying based on reviews.

---

## Installation

1. Clone this repository or download the files.
2. Install the required packages using pip:

```bash
pip install pandas numpy joblib nltk textblob streamlit scikit-learn
```

3. Make sure you have the following files in the same directory as `app.py`:

   * `file.csv` (dataset containing reviews and sentiment scores)
   * `poswords.csv` (optional: list of positive words)
   * `negwords.csv` (optional: list of negative words)
   * `review.joblib` (optional: pre-trained sentiment prediction model)

---

## Usage

To run the Streamlit app:

```bash
streamlit run app.py
```

* Select a product ID from the dropdown to see the reviews and sentiment analysis.
* Enter a custom review in the text box to predict its sentiment.
* The app highlights key positive and negative words to explain the sentiment.

---

## Dataset

The dataset for sentiment prediction can be found here:
[Amazon Reviews Dataset](https://www.kaggle.com/datasets/machharavikiran/amazon-reviews-2lak)

The dataset should have at least the following columns:

* `product_id` – Unique identifier for the product
* `product_title` – Name/title of the product
* `review_body` – Text of the review
* `sentiment_score` – Sentiment of the review (0 = negative, 1 = positive)

---

## Libraries Used

* `pandas` – For data manipulation.
* `numpy` – For numerical operations.
* `nltk` – For natural language processing.
* `textblob` – For sentiment analysis of individual words.
* `collections.Counter` – For counting most common sentiment labels.
* `scikit-learn` – For TF-IDF vectorization.
* `joblib` – For loading pre-trained models.
* `streamlit` – For building interactive web application.

---

## Notes

* Make sure `nltk` stopwords and corpora are downloaded if needed:

```python
import nltk
nltk.download('stopwords')
```

---

