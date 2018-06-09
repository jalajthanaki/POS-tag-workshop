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
               
               2.4 Why do we need to develop our own POS tagger?
    
---    

    Section 3. Build our own statistical POS tagger form scratch
       
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
       
## Dependencies 

* Python 3.3+

* Polyglot

* Spacy

* Py-CoreNLP (uses Stanford CoreNLP)

* NLTK

* Scikit-learn

* jupyter notebook


## Installation Instructions

### General instructions

* Set up python package manager [pip](https://pip.pypa.io/en/stable/quickstart/)
  
  * [Install pip for Windows](https://pip.pypa.io/en/stable/installing/) or [Install conda for Windows](https://conda.io/docs/user-guide/install/windows.html)
  
  * [Install pip for Linux](https://github.com/jalajthanaki/NLPython/blob/master/ch1/installation_guide/NLTK%2BSetup.md) or [Install conda for Linux](https://conda.io/docs/user-guide/install/linux.html)
  
  * [Install pip for Mac-OS](https://gist.github.com/haircut/14705555d58432a5f01f9188006a04ed) or [Install conda for Mac-OS](https://conda.io/docs/user-guide/install/macos.html)

* See: How to install python libraries [using conda](https://conda.io/docs/user-guide/tasks/manage-pkgs.html#installing-packages) 

* See: How to install python libraries [using pip](https://packaging.python.org/tutorials/installing-packages/#id16)

### For section 1:

* No dependency required for this section.


### For section 2: 

There are three dependencies are required.
---

2.1. [Polyglot](http://polyglot.readthedocs.io/en/latest/Installation.html#installing-upgrading-from-the-pypi)

2.2. [Stanford CoreNLP](https://stanfordnlp.github.io/CoreNLP/index.html#download) and [Py-CoreNLP](https://github.com/smilli/py-corenlp)

2.3. [Spacy POS tagger](https://spacy.io/usage/)

---

### Windows OS


**2.1. Polyglot**  

For installation refer this [link](https://github.com/aboSamoor/polyglot/issues/91)

    Step 1: $ git clone https://github.com/aboSamoor/polyglot.git
    
    Step 2: $ python setup.py install

    Step 3: Downloaded and pip install
            
            $ pip install pycld2-0.31-cp36-cp36m-win_amd64.whl
            
            $ pip install PyICU-1.9.8-cp36-cp36m-win_amd64.whl
            

**2.2. Stanford POS tagger**
    
__Step 1__: Install JDK 1.8 using this [link](https://www.guru99.com/install-java.html)
        
     
__Step 2__: Download Stanford CoreNLP from this [link](https://stanfordnlp.github.io/CoreNLP/index.html#download)

        Step 2.1: Download and extract the Stanford CoreNLP
        

__Step 3__: Start service of Stanford CoreNLP
        
        Step 1: cd ~/Path where you extract the Stanford CoreNLP
        
        Step 2: Run the server using all jars in the current directory (e.g., the CoreNLP home directory)
                
                $ java -mx4g -cp "*" edu.stanford.nlp.pipeline.StanfordCoreNLPServer -port 9000 -timeout 15000
        
__Step 4__: Setup Py-coreNLP
    

**2.3. Spacy POS tagger**
    
   __Step 1__: Documentation for Spacy is [here](https://spacy.io/usage/)
    
   __Step 2__: Run the installation commands
    
           $ sudo pip iinstall spacy
           
           $ sudo python3 -m spacy download en

---
### Linux OS

**2.1. Polyglot**  

    Step 1: sudo apt-get update
    Step 2: sudo apt-get install python-pyicu
    Step 3: sudo pip install pycld2  
    Step 4: sudo pip install Morfessor
    Step 5: sudo apt-get install python-numpy libicu-dev
    Step 6: sudo pip install PyICU
    Step 7: sudo pip install polyglot
   
**2.2. Stanford POS tagger**
    
 
__Step 1__: Install JDK 1.8
        
        Step 1.1: $ sudo mkdir /usr/lib/jvm
        
        Step 1.2: $ sudo tar xzvf jdk1.8.0_172.tar.gz -C /usr/lib/jvm
        
        Step 1.3: Set environment variable for java in .bashrc file
        
                  $ sudo vi ~/.bashrc or sudo gedit ~/.bashrc
        
        Step 1.4: Set path at the end of the bashrc file
        
                  JAVA_HOME=/usr/lib/jvm/jdk1.7.0_51
                  PATH=$PATH:$HOME/bin:$JAVA_HOME/bin
                  JRE_HOME=$HOME/bin:$JRE_HOME/bin
                  export JAVA_HOME
                  export JRE_HOME
                  export PATH

     
__Step 2__: Download Stanford CoreNLP from this [link](https://stanfordnlp.github.io/CoreNLP/index.html#download)

            Step 2.1: Download and extract the Stanford CoreNLP
        

__Step 3__: Start service of Stanford CoreNLP
        
            Step 1: cd ~/Path where you extract the Stanford CoreNLP
        
            Step 2: Run the server using all jars in the current directory (e.g., the CoreNLP home directory)
                
                    $ java -mx4g -cp "*" edu.stanford.nlp.pipeline.StanfordCoreNLPServer -port 9000 -timeout 15000
        
__Step 4__: Setup Py-coreNLP
            
            $ sudo pip install pycorenlp
          
           
__step 5__: Docker image (Instead of Step 1 to 4 above)

            docker run -p 9000:9000 --rm -it motiz88/corenlp       

**2.3. Spacy POS tagger**
    
   __Step 1__: Documentation for Spacy is [here](https://spacy.io/usage/)
    
   __Step 2__: Run the installation commands
    
               $ sudo pip iinstall spacy
               
               $ sudo python3 -m spacy download en


---        
    
###  Mac-OS

**2.1. Polyglot**  

    Step 1: sudo apt-get update
    Step 2: sudo apt-get install python-pyicu
    Step 3: sudo pip install pycld2  
    Step 4: sudo pip install Morfessor
    Step 5: sudo apt-get install python-numpy libicu-dev
    Step 6: sudo pip install PyICU
    Step 7: sudo pip install polyglot
   
**2.2. Stanford POS tagger**
    
Setup Standford CoreNLP
    
__Step 1__: Install JDK 1.8 [using this steps](http://www.cs.dartmouth.edu/~scot/cs10/mac_install/mac_install.html)
        
   
__Step 2__: Download Stanford CoreNLP from this [link](https://stanfordnlp.github.io/CoreNLP/index.html#download)

        Step 2.1: Download and extract the Stanford CoreNLP
        

__Step 3__: Start service of Stanford CoreNLP
        
        Step 3.1: cd ~/Path where you extract the Stanford CoreNLP
        
        Step 3.2: Run the server using all jars in the current directory (e.g., the CoreNLP home directory)
                
                $ java -mx4g -cp "*" edu.stanford.nlp.pipeline.StanfordCoreNLPServer -port 9000 -timeout 15000
        
__Step 4__: Setup Py-coreNLP

        Step 4.1: $ sudo pip install pycorenlp
    

**2.3. Spacy POS tagger**
    
   __Step 1__: Documentation for Spacy is [here](https://spacy.io/usage/)
    
   __Step 2__: Run the installation commands
    
               $ sudo pip iinstall spacy
               
               $ sudo python3 -m spacy download en




### For section 3: 

There are two dependencies are required.

---

3.1. NLTK

3.2. Scikit-learn

---


### Windows OS

**3.1 NLTK**
      
      Step 1: $ sudo pip install numpy scipy nltk
      
      Step 2: Download NLTK data
              
              $ python2 or python3
              
      Step 3: Inside python shell
              
              >>> import nltk
              
              >>> nltk.download()

**3.2 Scikit-learn**

      $ sudo pip install scikit-learn
      
 ---

### For Linux OS


**3.1 NLTK**
      
      Step 1: $ sudo pip install numpy scipy nltk
      
      Step 2: Download NLTK data
              
              $ python2 or python3
              
      Step 3: Inside python shell
              
              >>> import nltk
              
              >>> nltk.download()

**3.2 Scikit-learn**

      $ sudo pip install scikit-learn

---

### On Mac OS

**3.1 NLTK**
      
      Step 1: $ sudo pip install numpy scipy nltk
      
      Step 2: Download NLTK data
              
              $ python2 or python3
              
      Step 3: Inside python shell
              
              >>> import nltk
              
              >>> nltk.download()

**3.2 Scikit-learn**

      $ sudo pip install scikit-learn

---

#### Install jupyter notebook

* For installation you can refer [this link](http://jupyter.org/install)

* In anaconda jupyter notebook is built-in given. 

* You can install jupyter notebook by using following command
  
  `$ sudo pip install jupyter notebook`
  
* In order to start jupyter notebook execute the given command on cmd/terminal

  `$ jupyter notebook`

## Usage

* For Session 1: Use `Introduction_to_POS` ipython notebook

* For Session 2: Use `POS_tagger_Demo` ipython notebook

* For Session 3: Use `POS_from_scratch` ipython notebook

## Share this Git-Pitch Presentation 

See the Git-Pitch presentation using [this link](https://gitpitch.com/jalajthanaki/POS-tag-workshop/master?grs=github)


## Special Thanks

Thanks DataGiri/GreyAtom for hosting this event. 
