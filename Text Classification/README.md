
# Text Analysis

- Core of NLP
- Helps extract meaning, pattern and structured hidden in unstructured text data.
- Idea is to convert `text into numbers` so that powerful algorhitms can be applied

#### What Text Analysis includes
- Summarization
- Feature Extraction
- Sentiment Analysis [[Follow Here](https://github.com/MominAhmedShaikh/Natural-Language-Processing/tree/main/Text%20Classification/Sentiment%20Analysis)]
- Document Classification
- Topic Modelling
- Relationship Identification

#### Steps :point_down:

- `Load` Document or Corpus
- `Lower Case` all the Terms (Words) as Machine will not to able to differentiate between Apple and apple and it will take it as a seperate terms.
- `Check for` :point_down: (Remove if any)
  - Numbers
  - Punctuation marks
  - Stopwords 
- `Document Term Matrix (DTM)` - Describes the frequency of the terms that occur in a collection of documents.
  - **Need For DTM** - Representing text as a numerical structure is a common initial point for text mining, analytics such as search and ranking, creating taxonomies, categorization, document similarity, and text-based machine learning.
  
  <div style="width: 500px; margin: auto">
  <img src="https://www.mzes.uni-mannheim.de/socialsciencedatalab/article/advancing-text-mining/figures/dfm.png" align='center' alt="Description of image" width="700">
</div>

  - Also called Bag of words.
  - Perform DTM on :point_down:
  - **CountVectorizer**
       - Initiate CountVectorizer Object and Fit Transform Document or Corpus
       - *Drawbacks* 
         - Count of words irrespective of importance.
         - Just gives counts of words w.r.t a Document

  - **TF-IDF (term frequency-inverse document frequency)**
     - It takes into account not just the occurence of a term in a document but in the entire corpus.
     - *Formula*
     - <img src = 'https://miro.medium.com/max/816/1*1pTLnoOPJKKcKIcRi3q0WA.jpeg' width="275" height="100"/>
  - **N-grams** - Sequence of N Number of Words
  - Types 👇
       - `uni-gram` 
         - Initiate TF-IDF Vectorizer object and fit_transform on column.
         - Does not provide context on which the words are being used.
         - Example : If `fire` is considered as single word then it will not provide enough information, but if  `stick` is added to `fire` i.e. `fire stick` or `fire tv` or `fire hd`, it is providing some information about a product.
       - `bi-gram` - Initiate TF-IDF Vectorizer object and fit_transform on column, but select ngram_range (2,2) [min - 2 words , max - 2 words] 
       - `tri-gram` - Initiate TF-IDF Vectorizer object and fit_transform on column, but select ngram_range (3,4) [min -3 words , max - 4 words]
  - N-gram model - Predict occurance of N (word) based on N-1 (word)
       - Using Probability:
          - Find probability of word `you` after `Thank` will be given as 👇
              - `P(You | Thank) = P(# of times Thank you occurs)/P(# of time thank occurs)` 
  - Uses of N-grams
       - Feature generation for algorithms like NB,SVM,etc.
       - Creating auto-correct,auto-complete,speech recognition, etc.
  - Generating N-gram using NLTK
       - ```python3
             from nltk.util import ngrams
             sent = 'My Fight was delayed for an hour'
             n = 1 #2 - bigram , 3 - trigram
             unigrams = ngram(sentence.split(),n)
             for item in unigrams:
                print(item)
  <div style="width: 300px; margin: auto">
  <img src="https://devopedia.org/images/article/219/7356.1569499094.png" align='center' alt="Description of ngram" width="700">
</div>


  - Calculate `Sparcity`
       - High Sparcity :arrow_up: :infinity: :arrow_down: Less words frequency 
  
  
  
#### Feature Engineering on Textual Data
- ML Algorhithms expects numerical input for processes like Text or Doc classification.
- Various ways FE works on Textual Data as follows:
  - Check Number of Words in a Text
    - ```python3 
          df['num_words'] = df['text_col'].apply(lambda x : len(str(x).split()))
  - Check Number of Unique words in a Text
    - ```python3
          df['uniq_words'] = df['text_col'].apply(lambda x : len(set(str(x).split())))
  - Check Number of characters in a Text
    - ```python3
          df['num_char'] = df['text_col'].apply(lambda x : len((str(x)))
  

#### Glossary
- **Document :** Each line of text in the source is loaded document in the corpus. (kinda :wink: Statement)
- **Corpus :**  A Collection of Documents (kinda :wink: Paragraph)
- **Term :** Each word in a document 
- **Stopwords :** Are words so common that their information value is missing.
- **Document Term Matrix (DTM) or (TDM) :** Elements in this matrix represents the occurence of a Term.
- **Stemming :** Process of removing suffixes from words to get common origin.

