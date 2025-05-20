# Spam Filtering Using Bag Of Words
Spam emails or messages belong to the broad category of unsolicited messages received by a user.

Content of spam message can be specific keywords, links, or websites.

## Content Inspection
Contents of email or messages are english language sentences. Each sentences are collection of the organized collections of words.

Machine Language(ML) Algorithms can interpret and analyze numeric data. Each word in the content should be represented by numeric value.

### Tokenization
Tokenization is the process of breaking down a piece of text into smaller units, typically words.

Tokenization can be performed using NLTK.

## Split sentences
NLTK PUNKT is an unsupervised trainable tokenizer that splits text into sentences. You can install it with nltk.download('punkt'). PUNKT automatically recognizes abbreviations, acronyms, and sentence boundaries without manual annotation. You can train it on your own corpus to improve accuracy for domain-specific text. This tokenizer works across multiple languages and handles punctuation marks intelligently.

Download tokenizer
nltk.download("punkt")

# Tokenize the sentence into words
from nltk.tokenize import word_tokenize
words = word_tokenize(sentence)

### Get Unique words from sentences in content
This can be done by eliminating
1. Stop words
2. Non-alphabetic characters
3. Convert the words to lowercase

To identify the stop words use "from nltk.corpus import stopwords".

First get the list of stop words in English as follow
stop_words = set(stopwords.words("english"))

then remove stop words from the sentence
filtered_sentence = [word for word in words if word.lower() not in stop_words]

### Scoring words in the content
The free text of the content should be converted to a vector that we can use as input or output for a machine learning model.


