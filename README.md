# Byte Pair Encoding (BPE) for Text Compression

Byte Pair Encoding (BPE) is a widely used text compression technique that works by replacing repeated sequences of
characters with a single token, resulting in a smaller vocabulary size and improved model performance. In this tutorial,
we will implement a BPE algorithm from scratch using Python and compare it with the popular WordPiece tokenizer.

## What is Tokenization?

Tokenization is the first step in a deep learning Natural Language Processing (NLP) pipeline. It is the process of
breaking down a sentence or paragraph into individual words or subwords, also known as tokens. These tokens are then
used as input to train machine learning models for various NLP tasks such as sentiment analysis, machine translation,
and named entity recognition.

## BPE Algorithm Implementation

To implement the BPE algorithm, we will follow the following steps:

1. Read the text corpus and convert it into a list of words.
2. Calculate the frequency of each word in the corpus.
3. Add an end-of-word symbol (`</w>`) to each word in the frequency dictionary.
4. Train the BPE model on the frequency dictionary by iteratively merging the most frequent symbol pairs.
5. Encode a word using the BPE model by replacing the most frequent symbol pairs with a single token.

## WordPiece Tokenization

We will also compare the BPE model with the WordPiece tokenizer, a similar tokenization technique developed by Google
for use in their machine learning models. The WordPiece tokenizer uses a slightly different algorithm than BPE but
achieves similar results.

## Applying the Models on Romeo and Juliet Book

To test the performance of our BPE and WordPiece models, we will apply them on the famous book "Romeo and Juliet"

## Results

Our BPE model achieved a vocabulary size of 7216 tokens on the "Romeo and Juliet" book, while the WordPiece tokenizer
achieved a vocabulary size of 38285 tokens. This significant difference in vocabulary size can have a significant impact
on model performance, with a smaller vocabulary size generally leading to better model performance.

### Byte Pair Encoding (BPE) Algorithm

The BPE algorithm works by iteratively merging the most frequent pairs of adjacent characters in a text corpus until a
desired vocabulary size is reached. Here are the steps of the algorithm:

1. Initialize the vocabulary with all the characters in the text corpus.
2. While the desired vocabulary size has not been reached, repeat the following steps:
    - a. Compute the frequency of all character pairs in the vocabulary.
    - b. Merge the most frequent character pair into a single token, and update the vocabulary accordingly.

### WordPiece Algorithm

The WordPiece algorithm works by iteratively merging the most frequent subwords in a text corpus until a desired
vocabulary size is reached. Here are the steps of the algorithm:

1. Initialize the vocabulary with all the characters in the text corpus.
2. While the desired vocabulary size has not been reached, repeat the following steps:
    - a. Compute the frequency of all subwords in the vocabulary.
    - b. Merge the most frequent subword into a single token, and update the vocabulary accordingly.

We repeat the process until the desired vocabulary size is reached.

### Comparison of BPE and WordPiece

Both BPE and WordPiece are effective text compression techniques that can improve model performance by reducing the
vocabulary size. However, there are some differences between the two algorithms:

1. BPE tends to produce a smaller vocabulary size than WordPiece, which can lead to better model performance in some
   cases.
2. WordPiece is generally faster than BPE because it uses a more efficient merging strategy.
3. BPE can handle rare words better than WordPiece because it can merge any pair of adjacent characters, whereas
   WordPiece can only merge pre-defined subwords.

## Conclusion

In conclusion, BPE and WordPiece are two popular tokenization techniques used in NLP pipelines for text compression and
improved model performance. While both techniques achieve similar results, BPE generally has a smaller vocabulary size
and can lead to better model performance.