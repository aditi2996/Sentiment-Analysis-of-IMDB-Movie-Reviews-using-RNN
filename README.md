# Sentiment-Analysis-of-IMDB-Movie-Reviews-using-RNN
Performed sentiment analysis on 25,000 IMDB movie reviews to classify them as Positive or Negative. Built a Sequential RNN with 1.31M parameters, including 128D embeddings and a binary Dense output layer (sigmoid activation function). Utilized tokenization, padding, Adam optimizer, binary cross-entropy loss, and Early Stopping. 

# Detailed Description
# Objective:
  To develop a sentiment analysis model that classifies movie reviews as Positive or Negative, using the IMDB dataset.
# Steps Involved:

1.	Data Preparation:
      o	Dataset: 25,000 reviews, pre-labeled for sentiment classification.
      o	Vocabulary size: Restricted to the top 10,000 most frequent words.
      o	Review length: Standardized to 500 words using padding.
      o	Class distribution: Balanced dataset (50% Positive, 50% Negative).

2.	Exploratory Data Analysis:
      o	Analyzed review length distributions and vocabulary usage.
      o	Mapped numerical word indices to actual words for better interpretability.

3.	Model Design and Implementation:
        o	Built a Sequential Model with:
        	Embedding Layer: 128-dimensional word embeddings, 1,280,000 parameters.
        	SimpleRNN Layer: 32,896 parameters to capture sequential dependencies.
        	Dense Output Layer: Binary classification, 129 parameters.
        o	Total trainable parameters: 1.31M.
        o	Activation function: Sigmoid for binary sentiment prediction.

4.	Model Training:
      o	Optimizer: Adam.
      o	Loss function: Binary Cross-Entropy.
      o	Batch size: 32.
      o	Epochs: 10 (with Early Stopping at 5 patience epochs to prevent overfitting).
      o	Validation Split: 20% of training data used for validation.
      o	Training accuracy: 95.8%.
      o	Validation accuracy: 91.2%.
  	
6.	Model Evaluation and Deployment:
      o	Saved the trained model as simple_rnn_imdb.h5 for reuse.
      o	Tested on the held-out test dataset:
      	Test accuracy: 89.3%.
      	Model size: 5 MB.
  	
8.	Prediction Pipeline:
      o	Developed helper functions for:
      	Decoding Reviews: Converted numerical sequences back to human-readable text.
      	Preprocessing Input: Encoded and padded new reviews for predictions.
      o	Real-time prediction example:
      	Input: "This movie was fantastic! The acting was great and the plot was thrilling."
      	Predicted Sentiment: Positive.
      	Confidence Score: 81.15%.

