# Embeddings

This repository contains the word embeddings generated from Spanish corpora.

## Corpora used

* Scielo Full-Text in Spanish: We retrieved all the full-text available in Scielo.org (until December/2018) and processed them into sentences. 
* Wikipedia Health: We retrieved all articles from the following Wikipedia categories: Pharmacology, Pharmacy, Medicine and Biology.
* Scielo + Wikipedia Health: We concatenated the previous two corpora.

## Embeddings generated

Two different approaches were used: Word2Vec and fastText.

### Word2Vec

We used the python Gensim package (https://radimrehurek.com/gensim/index.html) to train different Word2Vect embeddings.
The following configurations were set:
* Embedding dimension: 50, 150 and 300.
* Epochs 15
* Window size: 10
* Minimum word count: 5
* Algorithm: CBOW
* Copora: Scielo, Wikipedia and Scielo + Wikipedia

### fastText

We used the fastText (https://fasttext.cc/) to train word embeddings.
We kept all standard options for training.
The following corpora were used: Scielo, Wikipedia and Scielo + Wikipedia

## Directory Structure

The example below shows the structure for the Wikipedia subset with 50 dimensions. All other subsets have the same structure
<pre>

./Wikipedia/Wikipedia_Fasttext.bin # Fasttext embedding in binary file
./Wikipedia/Wikipedia_Fasttext.vec # Fasttext embedding in text file
./Wikipedia/50/W2V_wiki_w10_c5_50_15epoch.txt # Word2Vec in text file
./Wikipedia/50/wiki_w10_c5_50_15epoch.w2vmodel # Word2Vec in gensim file
./Wikipedia/50/wiki_w10_c5_50_15epoch.w2vmodel.trainables.syn1neg.npy # Word2Vec in gensim file
./Wikipedia/50/wiki_w10_c5_50_15epoch.w2vmodel.wv.vectors.npy # Word2Vec in gensim file

</pre>

## Digital Object Identifier (DOI) and access to dataset files



## Contact

Felipe Soares (felipe.soares@bsc.es)


## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

Copyright (c) 2018 Secretaría de Estado para el Avance Digital (SEAD)
