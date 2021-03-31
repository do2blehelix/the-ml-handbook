---
layout: default
title: NLP
nav_order: 7
---

# Text Mining and NLP

**Applications**

* Sentiment Analysis
* Speech Recognition
* Chatbot
* Machine Translation (Google Translate)
* Spell Checking
* Keyword Search
* Information Extraction
* Advertisement Matching

NLP

##### NLU - Natural Language Understanding

* Mapping input to useful representations
* Analyzing different aspects of the language

##### NLG - Natural Language Generation

* Text planning
* Sentence planning
* Text realization

#### Ambiguities

* Lexical Ambiguity - Two or more possible meanings in a word.
  * She is looking for a **_match_** (matchstick vs partner)
  * The fisherman went to the **_bank_** (riverbank vs bank)
* Syntactic Ambiguity (aka structural/grammatical ambiguity) - Two or more possible meanings in a sentence or a sequence of words.
  * The chicken is ready to ear
* Referential Ambiguity - Referring to something using pronouns
  * The boy told his father about the theft. **_He_** was very upset.

### Processing text Terminologies

#### Tokenization

1st step is the process. Breaking the string into tokens, which are small structures.

1. Break a complex sentence into words
2. Understand the importance of each word
3. Produce a structural description on an input sentence.

Bigrams, Trigrams, and Ngram - Token of 2,3 or n number of words written together

#### Stemming

Normalize words into its base or root form by cutting prefixes or suffixes

Common Stemmers: Porter Stemmer (lenient) ; Lancaster Stemmer (aggressive) ; Snowball Stemmer (requires language input)

#### Lemmatization

Considers the morphological analysis of the word. Needs a detailed dictionary to link the word back to its lemma.

* Groups together different inflected forms of the word, called Lemma.
* Somehow similar to stemming as it maps several words to a common root.
* Output is a proper word

Eg **gone** **going** and **went** all maps to **go**