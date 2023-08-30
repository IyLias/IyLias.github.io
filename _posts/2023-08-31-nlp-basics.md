
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



<br><br>

## Stemming

The process for extracting "Stem". 

Stem(어간): 단어의 의미를 담고 있는 단어의 핵심 부분 






<br><br><br>

## Stopword

We remove some meaningless word tokens. 'meaningless' here directs words that occurs often but it's not useful for analyzing.


For example, I,my, me, over and etc are kind of stopwords. 





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