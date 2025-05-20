# Spam Filtering Using Bag Of Words
Spam emails or messages belong to the broad category of unsolicited messages received by a user.

Content of spam message can be specific keywords, links, or websites.

## Content Inspection
Contents of email or messages are english language sentences. Each sentences are collection of the organized collections of words.

Machine Language(ML) Algorithms can interpret and analyze numeric data. Each word in the content should be represented by numeric value.

## Split sentences
NLTK PUNKT is an unsupervised trainable tokenizer that splits text into sentences. You can install it with nltk.download('punkt'). PUNKT automatically recognizes abbreviations, acronyms, and sentence boundaries without manual annotation. You can train it on your own corpus to improve accuracy for domain-specific text. This tokenizer works across multiple languages and handles punctuation marks intelligently.

Download tokenizer
__*nltk.download("punkt")*__

## Tokenize the sentence into words
Tokenization is the process of breaking down a piece of text into smaller units, typically words.

Tokenization can be performed using NLTK.

__*from nltk.tokenize import word_tokenize*__

__*words = word_tokenize(sentence)*__

### Get Unique words from sentences in content
This can be done by eliminating
1. Stop words
2. Non-alphabetic characters
3. Convert the words to lowercase
4. Spelling Corrections

To identify the stop words use 
__*from nltk.corpus import stopwords*__

First get the list of stop words in English as follow

__*stop_words = set(stopwords.words("english"))*__

then remove stop words from the sentence

__*filtered_sentence = [word for word in words if word.lower() not in stop_words]*__

### Remove Non-alphabetic Caharacters 
__*text = re.sub('[^A-Za-z]', ' ', text)*__

### Convert the words to lowercase
__*text = text.lower()*__

### Spelling Corrections
__*from autocorrect import spell*__
__*text.append(spell(word))*__

### Scoring words in the content
The free text of the content should be converted to a vector that we can use as input or output for a machine learning model.


