# Biomedical Word Embeddings for Spanish: Development and Evaluation (v2.0)

This repository contains the second version of the word embeddings generated from Spanish corpora. In this version, we preprocessed the Corpora, obtaining better embeddings. 

## Digital Object Identifier (DOI) and access to files

https://doi.org/10.5281/zenodo.3744326

## Directory Structure

The example below shows the structure for the Wikipedia subset. All other subsets have the same structure:

<pre>
wikipedia/
    cbow/
	cased/
    		Wikipedia_cbow_cased.bin: fastText embedding in binary file.
        	Wikipedia_cbow_cased.vec: fastText embedding in text file.
	uncased/
    		Wikipedia_cbow_uncased.bin: fastText embedding in binary file.
        	Wikipedia_cbow_uncased.vec: fastText embedding in text file.
    skipgram/
	cased/
    		Wikipedia_skipgram_cased.bin: fastText embedding in binary file.
        	Wikipedia_skipgram_cased.vec: fastText embedding in text file.
	uncased/
    		Wikipedia_skipgram_uncased.bin: fastText embedding in binary file.
        	Wikipedia_skipgram_uncased.vec: fastText embedding in text file.	
</pre>

For usability and disk space reasons, the files in the directories are compressed in a ``tar.gz`` file. Uncompress only those embeddings you want to use.

## Corpora used

* **SciELO Full-Text in Spanish**: We retrieved all the full-text available in SciELO.org (until December/2018) and processed them into sentences. SciELO.org node contains all Spanish articles, thus includes Latin and European Spanish.
  * Sentences: 3,267,556
  * Tokens: 100,116,298
* **Wikipedia Health**: We retrieved all articles from the following Wikipedia categories: Pharmacology, Pharmacy, Medicine and Biology. Data were retrieved during December/2018.
  * Sentences: 4,030,833
  * Tokens: 82,006,270
* **SciELO + Wikipedia Health**: We concatenated the previous two corpora.


## Preprocessing Step

1) Removing not Spanish sentences using [Lingua](https://github.com/pemistahl/lingua) library.
	- It does not work with high accuracy for the Spanish language, thus we used a reversed way by removing English, German, French, Dutch and Danish sentences from our retrieved Spanish corpora.

2) Sentence splitting and tokenization using [Freeling](http://nlp.lsi.upc.edu/freeling/) toolkit.
   - **Freeling** (Padro and Stanilovsky, 2012) is a C++ library providing language analysis functionalities  (Morphological Analysis, Named Entity Detection, PoS-Tagging, Parsing, Word Sense Disambiguation, Semantic Role Labelling, so forth) for a variety of languages.

3) Final pre-processing using [Indra-Indexer](https://github.com/Lambda-3/Indraindexer) toolkit. 
   - Removing punctuations.
   - Replacing numbers for the place holder `<NUMBER>`.
   - Setting a minimum acceptable token size to 1.
   - Setting a maximum acceptable token size to 100.
   - Applying lowercase the tokens (we generated both cased and uncased versions).


**Corpora statistics after preprocessing**:

|Corpora|# Sentences|# Unique Tokens (Cased)|# Unique Tokens (Uncased)|
|--------|-----|------|------|
|SciELO|9,116,784|385,399|335,790|
|Wikipedia Health|4,623,438|255,057|222,954|
|SciELO + Wikipedia Health|13,740,222|503,647|435,652|


## Embeddings generation using fastText

We used [fastText](https://fasttext.cc/) to train the word embeddings.

We kept all standard options for training.

<pre>
- Minimum number of word occurrences: 5
- Phrase representation: No (i.e. length of word n-gram = 1)
- Minimum length of character n-gram: 3
- Maximum length of character n-gram: 6
- Size of word vectors: 300
- Epochs: 20
- Size of the context window: 5
- Word-Representation Modes: CBOW and Skip-gram
</pre>

We generated word embedding for both versions (cased and uncased corpora):
<pre>
- Wiki_cased
- Wiki_uncased
- Scielo_cased
- Scielo_uncased
- Scielo+Wiki_cased
- Scielo+Wiki_uncased
</pre>

## Evaluation

The evaluation of the original embeddings (version 1.0) was carried out by both extrinsically (with a Named Entity Recognition framework) and intrinsically, with the three already available datasets for such task UMNSRS-sim, UMNSRS-rel, and MayoSRS. In the NER scenario, we concluded that the best model was the one genenated using ``Skip-gram``, with 300 dimensions, and trained with SciELO and Wikipedia. We projected the words using Principal Component Analysis.

Further details about evaluation and the steps performed can be found in our paper: [Medical Word Embeddings for Spanish: Development and Evaluation](https://www.aclweb.org/anthology/W19-1916.pdf).

The PCA plots for our embeddings (version 1.0) and a general-domain embedding are available in this repository also:

* [Our embeddings](plots/our_embeddings.pdf)
* [SBWC embeddings](plots/sbwc_embeddings.pdf)

The translations for Spanish in TSV format of the UMNSRS and Mayo datasets one are also availabe in this Github repository:

* [UMNSRS Similarity](datasets/UMNSRS_Similarity_Filtered.tsv)
* [UMNSRS Relatedness](datasets/UMNSRS_Relatedness_Filtered.tsv)
* [Mayo](datasets/Mayo_Filtered.tsv)


### Evaluation of the new version

To evaluate the new version of the embeddings (version v2.0), we replicated the extrinsic evaluation from the original paper. The new embeddings outperform the previous ones by up to 1.68 points, while also solving some other minor issues.

[See results in the main README.md]

## Troubleshooting

If you get an ``Unicode/Decode error``, please load the embedding files adding a new argument to specify the encoding, as shown below:

<pre>
f = open(filename, "r", encoding="utf-8")
</pre> 


## Citing 
Please cite our paper if you use it in your experiments or project.

<pre>
@inproceedings{soares2019medical,
  title={Medical word embeddings for Spanish: Development and evaluation},
  author={Soares, Felipe and Villegas, Marta and Gonzalez-Agirre, Aitor and Krallinger, Martin and Armengol-Estap{\'e}, Jordi},
  booktitle={Proceedings of the 2nd Clinical Natural Language Processing Workshop},
  pages={124--133},
  year={2019}
}
</pre>


## Contact

Siamak Barzegar (siamak.barzegar@bsc.es)


## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

Copyright (c) 2020 Secretaría de Estado de Digitalización e Inteligencia Artificial (SEDIA)
