# Comp441-SentimentClassifier_NaiveBayes
1 Introduction
In this project you will implement a sentiment analysis system based on the “Large Movie Review
Dataset”. The input to your system is a piece of text and the output is a binary classification of the text
into “positive” or “negative”. Here are some examples:
Input: But perhaps you have to have grown up in the 80’s to truly appreciate this movie. If
you love the early 80’s this is definitely a must see. Also, one of the best soundtracks ever!
Output: Positive
Input: Widow hires a psychopath as a handyman. Sloppy film noir thriller which doesn’t
make much of its tension promising set-up.
Output: Negative
The core dataset contains 50,000 reviews split evenly into 25k train and 25k test sets. The overall
distribution of labels is balanced (25k pos and 25k neg). Feel free to use any preprocessing and prediction
method you like. Train on the training data and report your accuracy on the test data.
Please start by downloading and reviewing the data from
https://ai.stanford.edu/~amaas/data/sentiment
2 Preprocessing
You can explore the following ideas for preprocessing, they are all optional and not all may be helpful:
• Tokenize the text into individual words and punctuation.
• Lowercase the words.
• Map each unique token to an integer to ease further processing.
• Use an “unknown” symbol for tokens below a frequency threshold.
• Use only a subset of the words you deem informative as features.
• Crop longer texts and/or pad shorter texts to a fixed length.
3 Model
For prediction, you will implement a Naive Bayes Classifier. This classifier assumes the following generative process: To generate each (x, y) pair where y ∈ Y is a class and x = [x1, x2, . . . , xn] is a document
with features (e.g. words) xi ∈ X :
• First pick y ∈ Y with probability qy (categorical distribution).
• Then pick each word xi ∈ X with probability qxi|y (more categorical distributions).

