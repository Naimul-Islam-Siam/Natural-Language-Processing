## Bag of words
- First create tokens using tokenization
- Count up the frequency of the tokens
- The more frequent a word is, the more important it might be (can be a great way of determining the significance of word in a text)

## Preprocessing
- Lowercasing letters
- Stemming/Lemmatization --> Convert to root word
- Removing stop words and unwanted tokens
- Good experiment with different approaches and then decide according to which works the best for your need

## Gensim
Uses top academic models for complex tasks
- building a document or word vector
- topic identification and document comparison

**Word vectors** are multi-dimensional mathematical representations of words created using deep learning methods. They give us insight into relationships between words in a corpus.

**Corpus or Corpora(Plural):** A set of texts used to help perform nlp tasks

Genism uses a simple bag of words model which transforms each document into a bag of words using the token ids and the frequency of each tokens in the document.

Genism corpus is a list of lists, each list item representing one document. Each document is now a series of tuples, the first item representing the tokenid from the dictionary and the second item representing the frequency of the token in the document.

Unlike `Counter` based bag of words, `genism` models can easily be saved, updated and reused.


## TF-IDF

Term Frequency - Inverse Document Frequency

- Allows to determine the most important words in each document in a corpus
- Each corpus might have shared words beyond just stop words, these common words are like stop words and should be removed or at least down weighted in importance
- For example: In astronomy the word sky must be used a lot, but this word is not so important. So we downweight that

* So, TF-IDF ensures common words don't show up as keywords
* Keeps the document specific frequent words weighted high and the common words across the entire corpus weighted low