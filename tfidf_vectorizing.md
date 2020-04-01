# TFIDF and Word Vectorization
From my understanding, there is a lot of preprocessing that happens before vectorization.  First, you have to tokenize every word, then transform all the strings to lowercase.  Next you must remove stopwords (overly common and uninformative words) and punctuation, and finally join all those word tokens back together into one long string.  Now that preprocessed string can be fed into the vectorizer.  Fit and transform the vectoizer to your train data (your corpus) and then _just_ transform your test data (incoming/unseen data) with that same vectorizer.  The result should be an nd-array that you can coerce into a Pandas data frame.  This result matrix will have all of the words in your corpus as column names, and the rows will represent our documents, or new data, and will contain TFIDF scores of each word's significance, or rarity in the corpus.  My understanding is that, generally speaking, the higher the TFIDF score, the more rare that word is in the corpusm and therefor is more informative about the contents fo the document(s) it belongs to.  The TFIDF is calculated as </br>
</br>
      Wt,d = TFt,d log (N/DFt)</br>
</br>
Where...
- TFt,d is the number of occurrences of t in document d.
- DFt is the number of documents containing the term t.
- N is the total number of documents in the corpus.