# Fact Checking
The aim of this project is to use a Neural Network with some NLP techniques to achive a small portion of the fact checking problem, on the FEVER dataset.
As a matter of facts, the model tries to determine whether a given statement (fact) conveys a trustworthy information or not.

The focus of the project is on the **sentence embedding strategy** and the **merging strategies**

## Sentence embedding strategies
- Encode token sequences via a RNN and take the last state as the sentence embedding
- Encode token sequences via a RNN and average all the output states
- Encode token sequences via a simple MLP layer that flatten the 3D input tensor
- Compute the sentence embedding as the mean of its token embeddings (bag of vectors)

The RNN in this network is a bidirectional LSTM

## Merging strategies
- Concatenation: define the classification input as the concatenation of evidence and claim sentence embeddings
- Sum: define the classification input as the sum of evidence and claim sentence embeddings
- Mean: define the classification input as the mean of evidence and claim sentence embeddings
