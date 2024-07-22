# Binary Sentiment Classifier

## Overview

This project involves training a binary sentiment classifier using pre-trained transformer models from HuggingFace. The classifier is designed to distinguish between positive and negative sentiments based on a merged dataset from two sources: the `mteb/tweet_sentiment_extraction` dataset and the `stanfordnlp/imdb` dataset.

## Data

The project uses two datasets:

1. **`mteb/tweet_sentiment_extraction`**:
   - Contains tweets with sentiments labeled as positive, negative, or neutral.
   - Neutral sentiments are filtered out to focus on binary sentiment classification (positive and negative).

2. **`stanfordnlp/imdb`**:
   - Contains movie reviews with sentiments labeled as positive or negative.

### Data Processing

1. **Filter Neutral Sentiments**: The `mteb/tweet_sentiment_extraction` dataset is filtered to remove neutral sentiments.
2. **Label Mapping**: 
   - `0` for negative
   - `1` for positive

3. **Data Splitting**:
   - Train set
   - Validation set (10% of the train set)
   - Test set (separate from the merged dataset)

## Model

The sentiment classifier is built using pre-trained transformer models from HuggingFace. The model selection is based on efficiency and suitability for the task. 

### Model Training

1. **Architecture**: Chosen based on efficiency and effectiveness.
2. **Optimizer and Scheduler**: Defined based on best practices for training transformer models.
3. **Hyperparameters**: Adjusted to optimize performance, including the number of epochs, learning rate, and momentum.

### Training Loop

- Training and validation losses are tracked.
- Training and validation loss plots are generated to evaluate performance.

## Evaluation

1. **Test Set Accuracy**: The model's accuracy is reported on the test set.
2. **Example Predictions**: 10 example strings are tested to evaluate the model's performance on new data.

## Instructions

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/binary-sentiment-classifier.git
   cd binary-sentiment-classifier
