# Spam Classifier
Training a spam classifier on the Apache SpamAssassin datasets.

## Overview
I used the [Apache SpamAssassin public data](https://spamassassin.apache.org/old/publiccorpus/) to train a few classification models and picked the one with the best precision and recall. If you want to run this project, you only need the dependencies (see below); no extra files needed, the Jupyter notebook will download all the required files.

## Stages
- Download and understand the data format
- Split the data into training and test sets
- Prepare the data:
  - Remove email headers
  - Lowercase the email body
  - Convert urls to the word 'URL'
  - Convert numbers to the word 'NUM'
  - Remove punctuation
  - Convert the resulting text to bag-of-words representation (vector of counts of all words that appears in the training corpus)
- Train and evaluate a few models on recall, precision and ROC:
  - SGD
  - MLP
  - Decision Tree
  - Random Forest
  - AdaBoost
  - KNN
  - SVM classifier
- Fine-tune the best classifiers (MLP, AdaBoost and SVM)
- Evaluate on the test set

## Best Model
The best classifier is the MLP classifier with about:
- 98.7% accuracy
- 98.2% precision
- 98.9% recall

## Dependencies
- NumPy v1.16.2
- SciPy v1.2.1
- Scikit-Learn v0.20.3
- Matplotlib v3.0.2
- Joblib v0.13.2
