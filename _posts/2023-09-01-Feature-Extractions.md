---
layout: post
comments: true
title:  "basics of NLP: Feature Extraction"
date:   2023-09-01 
categories: [nlp]
---


We're gonna take a look how to deal with text data whose formats are mostly unstructured. Unstructured data cannot be represented in a tabular format. Therefore, it is essential to convert it into numeric features because most machine learning algorithms are capable of dealing only with numbers.


## Data Types

* Structured Data

    This is the most organized form of data. It is represented in tabular formats such as Excel files and CSV files.




* Semi-Structured Data

    This type of data is not presented in a tabular structure, but can be represented in a tabular format after transformation.

    Here, information is usually stored between tags following a definite pattern.
    XML, HTML files can be referred to as semi-structured data.




* Unstructured Data

    This type of data is the most difficult to deal with. Machine Learning algorithms would find it difficult to comprehend unstructured data without any loss of information.



<br><br>

## Data Cleaning


Often, extracting each token seperately does not help. In this case, the context in which these tokens are present becomes essential. Thus we consider n consecutive tokens at a time. 

n-grams refers to the grouping of n consecutive tokens together.


<br><br>

## General Features

General features refer to those that are not directly dependent on the individual tokens constituting a text corpus, such as the number of words, the number of occurrences of each part of speech, and the number of uppercase and lowercase words.


Here's the example code for extracting general features

```python
import pandas as pd
from textblob import TextBlob

df = pd.DataFrame([['The interim budget for 2019 will be announced on 1st February.'],
                   ['Do you know how much expectation the middle-class working population is having from this budget?'],
                   ['February is the shortest month in a year.'],
                    ['This financial year will end on 31st March.']

])


df.columns = ['text']
print(df)

df['number_of_words'] = df['text'].apply(lambda x: len(TextBlob(str(x)).words))
print(df['number_of_words'])

wh_words = set(['why', 'who', 'which', 'what', 'where', 'when', 'how'])
df['is_wh_words_present'] = df['text'].apply(lambda x: True if \
                                             len(set(TextBlob(str(x)).words).intersection(wh_words)) >0 else False)
print(df['is_wh_words_present'])

df['polarity'] = df['text'].apply(lambda x: TextBlob(str(x)).sentiment.polarity)
print(df['polarity'])

df['language'] = df['text'].apply(lambda x: TextBlob(str(x)).detect_language())
print(df['language'])
```






<br><br>

## Specific Features

* BoW: Bag of Words

    The output of this model for a set of text documents is a matrix. Each column of the matrix represents a word from the vocabulary and each row corresponds to one of these text documents.



* TF-IDF : Term Frequency-Inverse Document Frequency

    BoW model has a severe drawback. The frequency of occurrence of a token does not fully represent how much information it carries about a document.

    This is because a term occurring multiple times in many documents does not convey much information. Rare terms can carry much more information about the documents they are present in.

    TF-IDF is a method of representing text data in a matrix format using numbers that quantify how much information these terms carry in the given documents.

    