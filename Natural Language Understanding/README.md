# Natural Language Understanding (NLU)
Natural Language Understanding (NLU) is a subfield of Natural Language Processing (NLP) that helps computers understand and interpret human language. NLU focuses on the `semantics`, or `meaning`, of language, and is used in `voice and message` bots to process and understand human queries. 

While NLP can handle simple queries, NLU is `necessary for the computer to understand more complex or nuanced requests`. NLU is also used in s`entiment analysis` and `sarcasm detection`, as it allows computers to understand and interpret `complex emotions` and language use.

### Natural Language Understanding (NLU) involves three steps in understanding human language:
1. Language in context
   1. The system focuses on facilitating conversation between a voice bot and a human, understanding commands and simple exchanges of dialogue. 
   2. Example  :point_right:  Human: `"Play some jazz music."`
      Voice Bot: `"Sure, playing some jazz music now.`
      In this example, the voice bot understands the basic command `"play some jazz music"` and responds appropriately.
      
2. Compositional semantics
   1. NLU groups sentences together and tries to understand their collective meaning, such as the context of a group of food-related queries
   2. Example :point_right: Human: `"Show me the best recipes for a vegan dinner party."`
      Voice Bot: `"Here are some top-rated vegan dinner party recipes: [list of recipes]."`
      In this example, the voice bot groups the sentences together and understands the overall context of the conversation as being related to vegan food
      and dinner parties.
 
3. Lexical Semantics
   1. NLU studies the meaning of individual words and phrases, analyzing the meaning of each word in a sentence and combining them to understand the
   overall meaning of the sentence.
   2. Example :point_right: Human: `"I want something Mexican for lunch today."`
   Voice Bot: `"Here are some Mexican lunch options: [list of Mexican restaurants or dishes]."`
   In this example, the voice bot analyzes the individual words in the sentence and derives their meanings. It then combines the meanings of the words
   `"Mexican"` and `"lunch"` to understand the overall request for Mexican food for lunch and provides a list of options accordingly.
   
### Applications of Natural Language Understanding (NLU):

- **Chatbots and voice assistants:** NLU enables these systems to understand and interpret human language in order to respond appropriately.
- **Sentiment analysis:** NLU can be used to analyze text data and determine the sentiment (positive, negative, neutral) of the language used.
- **Sarcasm detection:** NLU can help identify sarcastic language and tone in text or speech.
- **Text classification:** NLU can be used to classify text data into predefined categories, such as spam detection or topic classification.
- **Summarization:** NLU can be used to automatically generate summaries of long text documents.
- **Question answering:** NLU can be used to build systems that can answer questions posed in natural language.
- **Language translation:** NLU can be used to translate text from one language to another.

### Bag of words
Bag of words is a representation of text data where the order of the words is ignored and `only the frequency of each word is taken` into account. It is commonly used in natural language processing and information retrieval systems.

To create a bag of words representation of a text, the following steps are typically followed:

- Tokenize the text: Split the text into individual words (also known as tokens).

- Remove irrelevant words: Remove stop words (such as "the", "a", "an"), punctuation, and other words that do not convey meaningful information.

- Count the occurrences of each word: Create a vocabulary of all the unique words in the text, and count the number of times each word appears.

- Create the bag of words representation: Create a vector with one dimension for each word in the vocabulary, and fill each dimension with the count of the corresponding word in the text.

For example, consider the following two sentences:

"The cat sat on the mat."

"The cat chased the mouse."

After tokenization and removing stop words, we would be left with the following vocabulary: ["cat", "sat", "mat", "chased", "mouse"]. The bag of words representation of these two sentences would be:

|Sentence|	cat|	sat|	mat|	chased	|mouse|
| :---  | :---:  | :---:  | :---:  | :---:  | :---:  |
|"The cat sat on the mat."|	1|	1	|1|	0|	0|
|"The cat chased the mouse."|1	|0	|0	|1	|1|


<p align="center"> 
<img src="https://github.com/MominAhmedShaikh/Natural-Language-Processing/blob/main/Natural%20Language%20Understanding/BOW.png" alt="Sentiment Analysis gif" height="600px">
</p>

Bag of words is a simple and efficient way to represent text data, but it ignores the order of words and any context they may have. Other approaches, such as n-grams or word embeddings, may be used to capture more contextual information.
