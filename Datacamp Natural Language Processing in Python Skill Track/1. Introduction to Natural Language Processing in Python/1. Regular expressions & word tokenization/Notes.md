## Tokenization

- Turning a string or document into tokens (smaller chunks)
- You can create own rules using RegEx
- Example:
  * breaking out words or sentences
  * separating # tag from tweets
  * removing all punctuations


### Why tokenize?
- Easier to map parts of speech
- Macthing common words
- Removing unwanted tokens (common words / repeated words)


### `nltk`
- `word_tokenize` tokenizes words (also includes punctuations) from sentence
- `sent_tokenize` tokenizes a document into sentences
- `regexp_tokenize` tokenizes a string or document based on a given regex
- `TweetTokenizer` specially used for tweets. Separates hashtags, mentions and exclamation points

`re.search()` vs `re.match()`
- `re.search` searches the entire word, and finds given pattern wherever it is in the word (if the pattern exists in the word in the first place)
- `re.match` searches the beginning, if the given pattern doesn't match with the beginning then it gives negative result


### Regex Ranges and Groups
Range is denoted using `[]` and Group is denoted using `()`

Groups are useful while defining an explicit group of characters.

- [A-Za-z]+ --> Upper and Lowercase English Alphabet
- [0-9] --> Numbers from `0` to `9`
- [A-Za-z\-\.]+ --> Upper and lowercase english alphabet including `-` and `.`
- (a-z) --> `a`, `-` and `z`
- (\s+|,) --> `spaces` or a `comma`