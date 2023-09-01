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



