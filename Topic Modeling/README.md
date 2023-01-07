# Topic Modeling

Topic modeling is a method for `automatically identifying the topics` that are discussed in a collection of documents. It works by `analyzing the words used` in the documents and `identifying groups of words` that `frequently` occur together, which are assumed to correspond to the main topics discussed in the documents. The resulting topics can be used to understand the main themes of the documents, to find relevant documents, or to summarize the content of the documents.

Using topic modeling, we could identify the main themes or topics discussed in the reviews, such as "quality," "price," "ease of use," and "customer service." we could then use these topics to understand what customers are generally saying about the product, or to identify areas where the product could be improved.

## Latent Dirichlet Allocation (LDA)
Latent Dirichlet Allocation (LDA) is a statistical model that is used to discover the underlying topics in a collection of documents. It does this by representing each document as a mixture of topics, and each topic is represented as a mixture of words.

For example, let's say we have a collection of documents about technology, politics, and sports. LDA might discover that one of the topics is about "smartphones," which would be represented as a mixture of words such as "iPhone," "Android," "Samsung," and so on. Another topic might be about "elections," which would be represented as a mixture of words such as "voting," "candidate," "campaign," and so on.

Here's a simple example of how LDA might work:

We have a collection of 3 documents, and we know that there are 2 topics: "smartphones" and "elections."
The first document is about the new iPhone and contains the words "iPhone," "Apple," "iOS," and "Face ID." LDA might represent this document as 60% "smartphones" and 40% "elections."
The second document is about the 2020 presidential election and contains the words "voting," "Trump," "Biden," and "campaign." LDA might represent this document as 50% "smartphones" and 50% "elections."
The third document is about the World Cup and contains the words "soccer," "team," "goal," and "match." LDA might represent this document as 0% "smartphones" and 100% "elections."
By analyzing the mixture of topics in each document, LDA can discover the underlying topics in the collection of documents and how they are related to each other.


Imagine we have a collection of 10 documents and we want to discover the underlying topics using LDA. The first step is to decide on the number of topics we want the model to discover. Let's say we decide on 2 topics for this example.

Next, we need to represent each document as a mixture of topics. In LDA, this is done using a type of probability distribution called a Dirichlet distribution. The Dirichlet distribution is a distribution over distributions, and it is parameterized by a vector of positive numbers called "alpha." Alpha determines the strength of the Dirichlet distribution and how peaked it is around the mean.

For each document, we draw a sample from the Dirichlet distribution to get the mixture of topics for that document. For example, if alpha is [0.5, 0.5] and we draw a sample [0.6, 0.4], this means that the document is 60% "topic 1" and 40% "topic 2."

Now that we have a way to represent each document as a mixture of topics, we need to represent each topic as a mixture of words. We do this using another type of probability distribution called a multinomial distribution. The multinomial distribution is a distribution over discrete outcomes (in this case, words) and is parameterized by a vector of probabilities for each outcome.

For each topic, we draw a sample from the multinomial distribution to get the mixture of words for that topic. For example, if the multinomial distribution for "topic 1" has the probabilities [0.1, 0.2, 0.3, 0.4] and we draw a sample [1, 0, 1, 2], this means that "topic 1" is made up of 1 occurrence of the first word, 0 occurrences of the second word, 1 occurrence of the third word, and 2 occurrences of the fourth word.

Now that we have a way to represent each topic as a mixture of words, we can use this information to infer the topics of each document. To do this, we use the mixture of topics for each document and the mixture of words for each topic to calculate the probability that a given word belongs to a given topic. We can then use this probability to assign each word in each document to the most likely topic.

For example, let's say that the mixture of topics for the first document is [0.6, 0.4] and the mixture of words for "topic 1" is [0.1, 0.2, 0.3, 0.4]. If the first document contains the words "apple," "banana," and "orange," we can calculate the probability that each of these words belongs to "topic 1" as follows:

"apple": 0.6 * 0.1 = 0.06
"banana": 0.6 * 0.2 = 0.12
"orange": 0.6 * 0.3 = 0.18
Since the probability is highest for "orange," we would assign the word "orange" to "topic 1" and the words "apple" and "banana" to "topic 2."

We repeat this process for each word in each document until all words have been assigned to a topic. This gives us the inferred topics for each document.

Finally, we can use this information to summarize the main topics in the collection of documents. For example, we might find that "topic 1" is about smartphones and "topic 2" is about elections.

- Topic Modeling using NLTK  :point_right: [View NoteBook](https://github.com/MominAhmedShaikh/Natural-Language-Processing/blob/main/Topic%20Modeling/Topic_Modeling.ipynb) or 👉 <a target="_blank" href="https://colab.research.google.com/github/MominAhmedShaikh/Natural-Language-Processing/blob/main/Topic%20Modeling/Topic_Modeling.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>
