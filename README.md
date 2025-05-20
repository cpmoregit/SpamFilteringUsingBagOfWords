# SpamFilteringUsingBagOfWords
Spam emails or messages belong to the broad category of unsolicited messages received by a user.

Content of spam message can be specific keywords, links, or websites.

## Content Inspection
Contents of email or messages are english language sentences. Each sentences are collection of the organized collections of words.

Machine Language(ML) Algorithms can interpret and analyze numeric data. Each word in the content should be represented by numeric value.

### Tokenization
Tokenization is the process of breaking down a piece of text into smaller units, typically words.

Tokenization can be performed using NLTK.

Import "word_tokeinze" from "nltk.tokenize"
from nltk.tokenize import word_tokenize

### Identify Unique words
We need to find the unique words in the content.

This can be done by eliminating
1. Stop words
2. Non-alphabetic characters
3. Convert the words to lowercase
4. Correct spelling

To identify the stop words use "from nltk.corpus import stopwords".

### Scoring words in the content
The free text of the content should be converted to a vector that we can use as input or output for a machine learning model.


