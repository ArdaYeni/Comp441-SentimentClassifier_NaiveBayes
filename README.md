# Sentiment Classification using Naive Bayes Classifier

This project implements a sentiment analysis system based on the **Large Movie Review Dataset**. The system classifies text into two categories: **positive** or **negative** sentiment using the **Naive Bayes Classifier**.

---

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Preprocessing](#preprocessing)
4. [Model Details](#model-details)
5. [Requirements](#requirements)
6. [How to Run](#how-to-run)
7. [References](#references)

---

## Introduction

The goal of this project is to classify movie reviews into **positive** or **negative** sentiment. Example outputs:

**Input:**  
*But perhaps you have to have grown up in the 80’s to truly appreciate this movie. If you love the early 80’s this is definitely a must see. Also, one of the best soundtracks ever!*  
**Output:** Positive  

**Input:**  
*Widow hires a psychopath as a handyman. Sloppy film noir thriller which doesn’t make much of its tension promising set-up.*  
**Output:** Negative  

---

## Dataset

The dataset contains **50,000 movie reviews**, evenly split into **25,000 training** and **25,000 test** reviews.  
- Reviews are balanced: 25,000 positive and 25,000 negative.  
- [Dataset Link](https://ai.stanford.edu/~amaas/data/sentiment)

---

## Preprocessing

Preprocessing techniques include:
- Tokenizing text into individual words and punctuation.
- Lowercasing words.
- Mapping each unique token to an integer.
- Handling low-frequency words with an "unknown" token.
- Cropping or padding texts to a fixed length.

These steps prepare the data for input into the Naive Bayes Classifier.

---

## Model Details

The Naive Bayes Classifier assumes the following process:
1. Select a class label \( y \) with probability \( q_y \).
2. Generate each word \( x_i \) based on \( q_{x_i | y} \).  

The probability of a document is given by:  
\[ P(x, y) = q_y \prod q_{x_i|y} \]  

### Key Features
- Add-one smoothing to avoid zero probabilities for unseen words.
- Independence assumption under the bag-of-words model.
- Minimum 80% accuracy required on the test set.

---

## Requirements

- **Model:** Naive Bayes Classifier (no alternatives).
- **Language:** Python (use only `NumPy`; no other libraries allowed).
- **Data:** Raw dataset only (no preprocessed files like `imdb.vocab`).
- **Performance:** Runtime under 1 minute on a regular workstation.
- **Accuracy:** At least 80% on the test set.

---

## How to Run

1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
