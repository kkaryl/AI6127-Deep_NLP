# AI6127: Assignment 1

Topic: Language Model

Questions:

1. Show derivation of Softmax gradient update formula.
2. Develop a neural language model in PyTorch

## Q2 Develop a neural language model in PyTorch

Dataset: [wikitext-2](https://s3.amazonaws.com/research.metamind.io/wikitext/wikitext-2-v1.zip)

The dataset for this exercise will be the wikitext-2 dataset. You can use this [code](https://github.com/pytorch/examples/blob/master/word_language_model/main.py) as your codebase
and build on top of it. Please do the following:

- [x] Please download the dataset and the code. The dataset should have three files: *train*, *test*, and
  *valid*. The code should have basic prepossessing (see data.py) and data loader (see main.py)
  that you can use for your work. Try to run the code.
- [x] You should understand the preprocessing and data loading functions.
- [x] Write a class class *FNNModel(nn.Module)* similar to class *RNNModel(nn.Module)*. The FNNModel
  class should implement a language model with a feed-forward network architecture.
  For your reference, RNNModel implements a recurrent network architecture, more specifically,
  Long Short-Term Memory (LSTM) that you will learn later in the course.
  The FNN model should have an architecture as shown in Figure 1. This is indeed the first
  neural language model [1]. The neural model learns the distributed representation of each
  word (embedding look-up matrix C) and the probability function of a sequence as a function
  of the distributed representations. It has a hidden layer with tanh activation and the output
  layer is a Softmax layer. The output of the model for each input of (n - 1) previous word
  indices are the probabilities of the |V| words in the vocabulary.
- [x] Train the model with any of SGD variants (Adam, RMSProp, Adagrad).
- [x] Show the perplexity score on the test set. You should select your best model based on the
  perplexity score on the valid set.
- [x] Do steps (iv)-(v) again, but now with sharing the input (look-up matrix) and output layer
  embeddings (final layer weights).
- [x] Adapt generate.py so that you can generate texts using your language model (FNNModel).
- [x] In your opinion, which computation/operation is the most expensive one in inference or forward
  pass? Can you think of ways to improve this? If yes, please mention.
- [x] Notice that the model also learns word vectors (input and output layer embeddings) as a
  byproduct. One way to evaluate the trained word vectors is to measure the cosine similarity
  between pairs of words, and then report the correlation with the similarity scores given by
  humans. For this exercise, use the dataset available here and report the Spearman correlation
  for the input embeddings. Exclude any pair if it is not in the embedding matrix.

## References

Bengio, Yoshua, et al. "A neural probabilistic language model." *Journal of machine learning research* 3.Feb (2003): 1137-1155.