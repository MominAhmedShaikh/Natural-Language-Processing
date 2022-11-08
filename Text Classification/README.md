
# Text Analysis

- Core of NLP
- Helps extract meaning, pattern and structured hidden in unstructured text data.
- Idea is to convert `text into numbers` so that powerful algorhitms can be applied

#### What Text Analysis includes
- Summarization
- Feature Extraction
- Sentiment Analysis
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
- `Document Term Matrix (DTM)`
  - Initiate CountVectorizer Object and Fit Transform Document or Corpus
- Calculate `Sparcity`
  - 1 

#### Glossary
- **Document :** Each line of text in the source is loaded document in the corpus. (kinda :wink: Statement)
- **Corpus :**  A Collection of Documents (kinda :wink: Paragraph)
- **Term :** Each word in a document 
- **Stopwords :** Are words so common that their information value is missing.
- **Document Term Matrix (DTM) or (TDM) :** Elements in this matrix represents the occurence of a Term.
- **Stemming :** Process of removing suffixes from words to get common origin.
