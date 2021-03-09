# Assignment 2 - CS 772 
[ View in Colab ](https://colab.research.google.com/drive/1BPJAgBfmdPjaf9lJgypwO9Fpg_32wVaQ?usp=sharing)
### Problem Definition
* Perform Sentiment analysis on the given text data to determine a review score from 1-5.
* Convert text data into usable format for ml algorithm
* Predict ratings for reviews by use of FFNN, then fine tuning various parameters such as number of hidden layers, activation function, etc. 
* Manage the problem of data imbalance (oversample, undersample, weighted loss)
* Achieve good results accuracy >80%


### System Architecture

* Simple feed forward neural network, with varied hidden layer assemblies whose Input is text and Output is Probability score out of 5 classes
* Using 3 different word representation techniques namely, Word2Vec, Glove, Fasttext
* Using Dropout layers with 20% probability to reduce overfitting

#### Overview of architecture:

Data -> embedding matrix -> Data encoding -> Neural Network -> Prediction 

### Performance
The best test scores we obtained in respective embedding methods chosen and addressing data imbalance by oversampling. 
|Model|F1 score|Accuracy|
|:-----|:-----|:------|
|Word2vec|0.59|0.63|
|Glove|0.59|0.63|
|FastText|0.68|0.60|

### Best Confusion matrix and model summary
  
||1|2|3|4|5|
|---|:----|:-----|:-----|:-----|:-----|
|1|715|173|126|55|202|
|2|206|89|119|56|160|
|3|155|91|230|137|198|
|4|77|49|194|297|787|
|5|169|86|241|609|4679|

* Representation: Word2Vec
* Architecture: 512,256
* Data balancing: Weighted loss
* Activation: Relu















