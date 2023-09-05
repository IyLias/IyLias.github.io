---
layout: post
comments: true
title:  "basics of NLP: Text Preprocessing"
date:   2023-08-31 
categories: [nlp]
---

To use texts as we want, we need Text Preprocessing. <br>
Let's take a look some processes. 


## Tokenization 

To do some work, we divide all sentences into unit, which is called a token. 


When we set its standard as a word, it's called "word tokenization"
and also can be as a sentence.

When it comes to dealing with Korean, it's not enough to use spacing for tokenization.

As words are combined with postpositions in many cases, we should detach these also. 

We should understand the word "morpheme". It means that the smallest unit which has meaning. It has two types, which are independent morpheme and dependent morpheme.

* 자립 형태소 : 접사, 어미, 조사와 상관없이 자립하여 사용할 수 있는 형태소. 그 자체로 단어가 된다. 체언(명사, 대명사, 수사), 수식언(관형사, 부사), 감탄사 등이 있다.

* 의존 형태소 : 다른 형태소와 결합하여 사용되는 형태소. 접사, 어미, 조사, 어간을 말한다.


As in the example above, individual tokens extracted one by one like words are referred to as "unigrams."

But we can also extract two or three tokens at the same time. If we extract two tokens at a time, it is called bigrams and if three tokens, it is called trigrams.

Based on the requirements, n-grams can be extracted.



<br><br>

## PoS : Parts of Speech

PoS tagging refers to the process of tagging words within sentences into their respective parts of speech and then finally labeling them. 







<br><br>

## Stemming

The process for extracting "Stem". <br>
More specifically, "Stemming" means that the process of restoring the original form of a word.

Stem(어간): 단어의 의미를 담고 있는 단어의 핵심 부분 




<br><br>

## Lemmatization

Sometimes the stemming process leads to inappropriate results. To overcome these problems with stemming, we make use of lemmatization. 

In this process, an additional check is being made, by looking through the dictionary to extract the base form of a word.







<br><br><br>

## Stopword

Stop words are common words that are just used to support the construction of sentences.

We remove some meaningless word tokens. 'meaningless' here directs words that occurs often but it's not useful for analyzing.


For example, I,my, me, over and etc are kind of stopwords. 

Here's the result of using nltk stop words

['i', 'me', 'my', 'myself', 'we', 'our', 'ours', 'ourselves', 'you', "you're", "you've", "you'll", "you'd", 'your', 'yours', 'yourself', 'yourselves', 'he', 'him', 'his', 'himself', 'she', "she's", 'her', 'hers', 'herself', 'it', "it's", 'its', 'itself', 'they', 'them', 'their', 'theirs', 'themselves', 'what', 'which', 'who', 'whom', 'this', 'that', "that'll", 'these', 'those', 'am', 'is', 'are', 'was', 'were', 'be', 'been', 'being', 'have', 'has', 'had', 'having', 'do', 'does', 'did', 'doing', 'a', 'an', 'the', 'and', 'but', 'if', 'or', 'because', 'as', 'until', 'while', 'of', 'at', 'by', 'for', 'with', 'about', 'against', 'between', 'into', 'through', 'during', 'before', 'after', 'above', 'below', 'to', 'from', 'up', 'down', 'in', 'out', 'on', 'off', 'over', 'under', 'again', 'further', 'then', 'once', 'here', 'there', 'when', 'where', 'why', 'how', 'all', 'any', 'both', 'each', 'few', 'more', 'most', 'other', 'some', 'such', 'no', 'nor', 'not', 'only', 'own', 'same', 'so', 'than', 'too', 'very', 's', 't', 'can', 'will', 'just', 'don', "don't", 'should', "should've", 'now', 'd', 'll', 'm', 'o', 're', 've', 'y', 'ain', 'aren', "aren't", 'couldn', "couldn't", 'didn', "didn't", 'doesn', "doesn't", 'hadn', "hadn't", 'hasn', "hasn't", 'haven', "haven't", 'isn', "isn't", 'ma', 'mightn', "mightn't", 'mustn', "mustn't", 'needn', "needn't", 'shan', "shan't", 'shouldn', "shouldn't", 'wasn', "wasn't", 'weren', "weren't", 'won', "won't", 'wouldn', "wouldn't"]




<br><br><br>


## Text Normalization

Text Normalization is a process wherein different variations of text get converted into a standard form. 

Ex) does, doing => do








<br><br><br>

## Padding


There can be length of each sentence is different. 

However, machines can consider documents with the same length as a single matrix and process them together. In other words, there are times when we need to align the lengths of multiple sentences arbitrarily for parallel operations.



<br><br><br>

## One-Hot Encoding


Here's the simple code for One-Hot Encoding. 

```python
def one_hot_encoding(word, word_to_index):
  one_hot_vector = [0]*(len(word_to_index))
  index = word_to_index[word]
  one_hot_vector[index] = 1
  return one_hot_vector
```

The problem for One-Hot Encoding is that as the number of words increases, this expression method has a disadvantage of requiring more space to store vectors. Another way to express this is that the dimension of the vector increases. One-hot vectors have a dimensionality equal to the size of the vocabulary.