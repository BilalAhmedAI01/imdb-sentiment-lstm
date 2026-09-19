# IMDB Sentiment Classification — LSTM & Bidirectional LSTM

A beginner-friendly notebook comparing **LSTM** and **Bidirectional LSTM** architectures for sentiment classification on the IMDB movie review dataset, built with TensorFlow/Keras.

## Overview
- **Dataset:** IMDB movie reviews (25,000 train / 25,000 test), limited to the top 10,000 most frequent words, reviews padded/truncated to 200 tokens.
- **Models compared:**
  - `Embedding → LSTM(32) → Dense(1, sigmoid)`
  - `Embedding → Bidirectional(LSTM(32)) → Dense(1, sigmoid)`
- Both trained for 5 epochs, batch size 128, with a 20% validation split, under identical settings for a fair comparison.

## Results

| Model | Test Accuracy |
|---|---|
| LSTM | 85.38% |
| Bidirectional LSTM | 86.19% |

## What's inside
- Step-by-step markdown explanations before every code cell
- Side-by-side model comparison
- Custom sentence testing, including a mixed-signal example ("the movie despite a slow start was excellent") designed to highlight where bidirectional context helps

## Requirements
- TensorFlow 2.x
- Runs directly in Google Colab — no local setup needed

## Notes
Short custom test sentences (6–8 words) can occasionally be misclassified, since both models were trained on full-length reviews (up to 200 words). This is an expected limitation of the small model/short training run, not a bug.
