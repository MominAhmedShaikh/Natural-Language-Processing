# Sentiment Analysis Using VADER

- Valance aware dictionary and sentiment reasoner `VADER`
- VADER uses combination of `sentiment lexicon` in a list of lexical features (eg. words) which are generally labelled according to their sentiment orientation.
- VADER not only tells Positivity and Negativity of a sentence but also how Positive and Negative it is.

### Advantages of VADER
- Comfortable to any domain especially Social media type texts.
- Fast enough to be used online with data stream.
- Does not require any training.

### Key points in VADER
- Punctuation 
   - Use of `(!) marks` increses the magnitude of sentiment but to some extent. 
- Capitalization
   - More magnitude is given when Capitalized words are used. eg. `GREAT > great`
- Degree modifiers
   - Also called identifiers can increase or decrease magnitude of a sentiment.
   - eg. the service was `extremely` good > the service was good > the service was `marginally` good.
- Conjunction 
   - Use of Conjunction such as `but` shifts the magnitude.
   - eg. The service was good `but` it can be better. 
   - Half part conveys Positive sentiment but latter half conveys Negative sentiment. 
- Handling `Emojis , Slangs , Emoticons`

### Different Libraries for Sentiment Analysis

- Sentiment Analysis using VADER   :point_right: <a target="_blank" href="https://colab.research.google.com/github/MominAhmedShaikh/Natural-Language-Processing/blob/main/Text%20Classification/Sentiment%20Analysis/Sentiment%20Analysis%20Using%20VADER/Sentiment_Analysis_Using_VADER.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>  or   :point_right: [View NoteBook](https://colab.research.google.com/github/MominAhmedShaikh/Natural-Language-Processing/blob/main/Text%20Classification/Sentiment%20Analysis/Sentiment%20Analysis%20Using%20VADER/Sentiment_Analysis_Using_VADER.ipynb)
</a>
