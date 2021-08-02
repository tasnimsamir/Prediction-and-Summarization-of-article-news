# Predication and summarizing for news article

## Summary about project:
### When user enter his/her text (article, book,...), the program will summarizes the text using two different models which are:
1. Latent Semantic Analysis model (LSA):
* It is an efficient technique for extracting out the hidden context of the document, ang the the relations between term in document.
* Reduce the dimensionality of the original text-based dataset.
* It helps us understand what each topic is encoding.
* Find relations between terms.
2. Bert model
* It is a a bidirectional pretrained model.

### And then we use a clustering and classification models to tell user which type of news is it.
* Entertainment
* Health
* Business
* Technology

### The used clustering model is:
* K-means
### The used classification models are:
* Random forest classifiers
* Logistic regression classifiers
* Naïve bayes classifiers
* The best model of them in performance is (Logistic regression classifiers with BOW)

## Detailed steps:
1. Get some atricles in the previous topics, and manual summarization to compare it with the summarization models results.

2. Apply data processing on the text using:
* Removing tags,
* Removing punctuation,
* Removing multiple whitespaces,
* Removing stopwords,
* Applying lemmatization, and
* Appling lower case
3. Then applying feature engineering:
* Bow (Bag-of-words)
* TF-IDF (term frequency-inverse document frequency)
4. Then apply classification with labeled data (Entertainment, Health, Business, Technolog)
5. Apply clustering on the data whitout labeling.
6. Aplly summarization models (LSA, BERT)
7. Calculate the similarity between the manual summarization and the summarization of (LSA, BERT) using Spacy.
8. Get the similarity result and it was:
* 99% with LSA
* 16% with BERT
* LSA model has a shorter and more meaningful summary than BERT
