# All about Part of Speech (POS) tags


**Understanding of POS tags and build a POS tagger from scratch**

This repository is basically provides you basic understanding on POS tags. I have tried to build the custom POS tagger using Treebank dataset.

---

## Workshop Outline

There are main three sections here.
---
    Section 1. Introduction to Part of Speech tags
    
              1.1 What is Parts of Speech?

              1.2 What is Parts of Speech tagging?

              1.3 What is Part of Speech tagger?

              1.4 What are the various types of the Part of Speech tags?

              1.5 Which applications are using POS tagging?

---
       
    Section 2. Generate Part of Speech tags using various python libraries
       
               2.1 Generating POS tags using Polyglot library
       
               2.2 Generating POS tags using Stanford CoreNLP 
       
               2.3 Generating POS tags using Spacy library
    
---    

    Section 3. Build our own POS tagger form scratch
       
               3.1 Import dependencies

               3.2 Explore dataset

                    3.2.1 Explore Brown Corpus

                    3.2.2 Explore Penn-Treebank Corpus

                3.3 Generate features

                3.4 Transform Dataset

                3.5 Build training and testing dataset       

                3.6 Train model

                3.7 Measure Accuracy

                3.8 Generate POS tags for given sentence
       

## Installation Instructions

### For section 1:

* No dependency required for this section.

### For section 2: 

There are three dependencies are required.
---
1. Polyglot library

2. Stanford POS tagger and Py-CoreNLP

3. Spacy POS tagger

---

    Step 1: sudo apt-get update
    Step 2: sudo apt-get install python-pyicu
    Step 3: sudo pip install pycld2
    Step 4: sudo pip install PyICU
    sudo pip install Morfessor
    Step 5: sudo apt-get install python-numpy libicu-dev
    Step 6: sudo pip install polyglot

Stanford POS tagger

    https://nlp.stanford.edu/software/tagger.html
    https://stanfordnlp.github.io/CoreNLP/
    https://github.com/smilli/py-corenlp
    https://stanfordnlp.github.io/CoreNLP/corenlp-server.html#getting-started

Spacy POS tagger

    https://spacy.io/usage/
    sudo pip iinstall spacy
    sudo python3 -m spacy download en



### For section 3: 

There are two dependencies are required.
---
1. NLTK

2. Scikit-Learn
---


## Usage

* For Session 1: Use `Introduction_to_POS` ipython notebook

* For Session 2: Use `POS_tagger_Demo` ipython notebook

* For Session 3: Use `POS_from_scratch` ipython notebook

