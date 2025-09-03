
# Natural Language Processing (NLP)

## Introduction

Field of AI that allow computers to UNDERSTAND, INTERPRET and GENERATE human language data  

### Techniques used to PROCESS and ANALYZE human language data
1. Statistics
2. Machine Learning
3. Deep Learning

### NLP in daily life
1. Email
- automatically detect spam emails
2. Chatbots or Customer Support Systems
- understand and respond to customer queries

### Supervised vs Unsupervised NLP

| Supervised Learning | Unsupervised Learning |
|---------------------|-----------------------|
| Requires LABELED data for training | Works with UNLABELED data |
| Training an algorithm to learn the relationship between the INPUT and an OUTPUT | Identify patterns or group similar items together |

## Text Preprocessing

### Importance
If feeding an algorithm with garbage data, the results will be garbage as well. (accuracy down, performance issues)
Garbage in, garbage out (GIGO).  

### Steps
1. General Cleaning
- *organizing*
- *tidying up* the text
- remove anything *that can throw an error*

2. Removing noise from data set
- remove aspects in the data *that are not adding value*

3. Getting the data in the right format for the ML algorithm

### Lowercase
helps maintain consistency in our data and outputs  

```python
sentence = "Her cat's name is Luna"
lower_sentence = sentence.lower()
print(lower_sentence)
```
> her cat's name is luna

```python
sentence_list = ['Could you pass me the TV remote?',
                 'It is IMPOSSIBLE to find this hotel',
                 'Wasnt to go for dinner on Tuesday?']

lower_sentence_list = [x.lower() for x in sentence_list]
print(lower_sentence_list)
```

### Removing stop words
stop words -> common words in the language *that don't carry much meaning* 
to remove complexity from the data  
use NLTK package to remove stop words  (and, of, a, the)  

```python
import nltk
nltk.download()
```
> Downloading package NLTK

```python
from nltk.corpus import stopwords
en_stopwords = stopwords.words('english')
print(en_stopwords)
```
> ['a', 'about', 'above', 'after', 'again', 'against', 'ain', 'all', 'am', 'an', 'and', 'any', 'are', 'aren', "aren't", 'as', 'at', 'be', 'because', 'been', 'before', 'being', 'below', 'between', 'both', 'but', 'by', 'can', 'couldn', "couldn't", 'd', 'did', 'didn', "didn't", 'do', 'does', 'doesn', "doesn't", 'doing', 'don', "don't", 'down', 'during', 'each', 'few', 'for', 'from', 'further', 'had', 'hadn', "hadn't", 'has', 'hasn', "hasn't", 'have', 'haven', "haven't", 'having', 'he', "he'd", "he'll", 'her', 'here', 'hers', 'herself', "he's", 'him', 'himself', 'his', 'how', 'i', "i'd", 'if', "i'll", "i'm", 'in', 'into', 'is', 'isn', "isn't", 'it', "it'd", "it'll", "it's", 'its', 'itself', "i've", 'just', 'll', 'm', 'ma', 'me', 'mightn', "mightn't", 'more', 'most', 'mustn', "mustn't", 'my', 'myself', 'needn', "needn't", 'no', 'nor', 'not', 'now', 'o', 'of', 'off', 'on', 'once', 'only', 'or', 'other', 'our', 'ours', 'ourselves', 'out', 'over', 'own', 're', 's', 'same', 'shan', "shan't", 'she', "she'd", "she'll", "she's", 'should', 'shouldn', "shouldn't", "should've", 'so', 'some', 'such', 't', 'than', 'that', "that'll", 'the', 'their', 'theirs', 'them', 'themselves', 'then', 'there', 'these', 'they', "they'd", "they'll", "they're", "they've", 'this', 'those', 'through', 'to', 'too', 'under', 'until', 'up', 've', 'very', 'was', 'wasn', "wasn't", 'we', "we'd", "we'll", "we're", 'were', 'weren', "weren't", "we've", 'what', 'when', 'where', 'which', 'while', 'who', 'whom', 'why', 'will', 'with', 'won', "won't", 'wouldn', "wouldn't", 'y', 'you', "you'd", "you'll", 'your', "you're", 'yours', 'yourself', 'yourselves', "you've"]

```python
sentence = "it was to far to go to the shop and he did not want her to walk"
sentence_no_stopwords = ' '.join([word for word in sentence.split() if word not in en_stopwords])
print(sentence_no_stopwords)
```
> far go shop want walk

```python
if 'did' in en_stopwords:
    en_stopwords.remove('did')
    
if 'not' in en_stopwords:
    en_stopwords.remove('not')

en_stopwords.append('go')
```

```python
sentence_no_stopwords_custom = ' '.join([word for word in sentence.split() if word not in en_stopwords])
print(sentence_no_stopwords_custom)
```
> far shop did not want walk

### Regular expressions
`\n` => Enter  
`\t` => Tab  
`\\` => Backslash  

#### Raw strings
`r""` => raw string, ignore escape characters  
```python
import re
my_folder = r"C:\desktop\notes"
print(my_folder)
```
> C:\desktop\notes

#### Searching for a pattern (`re.search`)
```python
result_search = re.search("pattern", r"string to contain the pattern")
print(result_search)
```
> <re.Match object; span=(22, 29), match='pattern'>

#### Verifying the result
```python
text = "string to contain the pattern"
print(text[22:29]) 
```
> pattern

#### Not finding a pattern
```python
result_search_2 = re.search("pattern", r"the phrase to find isn't in this string")
print(result_search_2)
```
> None

#### Replacing a pattern (`re.sub`)
```python
string = r"sara was able to help me find the items I need quickly"
new_string = re.sub("sara", "sarah", string)
print(new_string)
```
> sarah was able to help me find the items I need quickly

#### Search from list of strings (`re.search`) in `list`
```python
customer_reviews = ["sam was a great help to me in the store",
                    "the cashier was very rude to me, I think her name was eleanor",
                    "amazing work from sadeen!",
                    "sarah was able to help me find the items that I need quickly",
                    "lucy is such a great addition to the team",
                    "great service from sara she found me what i wanted"]

sarah_reviews = []
pattern_to_find = r"sarah?"

for string in customer_reviews:
    if (re.search(pattern_to_find, string)):
        sarah_reviews.append(string)
    
print(sarah_reviews)
```
> ['sarah was able to help me find the items I needed quickly', 'great service from sara she found me what i wanted']

#### Caret operator (`^`)  
indicates the `start` of a string  
```python
a_reviews = []
pattern_to_find = r"^a"

for string in customer_reviews:
    if re.search(pattern_to_find, string):
        a_reviews.append(string)

print(a_reviews)
```
> ['amazing work from sadeen!']

#### Dollar operator (`$`)  
indicates the `end` of a string  
```python
y_reviews = []
pattern_to_find = r"y$"

for string in customer_reviews:
    if re.search(pattern_to_find, string):
        y_reviews.append(string)

print(y_reviews)
```
> ['sarah was able to help me find the items I needed quickly']

#### Pipe/Alternation operator (`|`)  
search more than one words  
```python
needwant_reviews = []
pattern_to_find = r"(need|want)ed"

for string in customer_reviews:
    if re.search(pattern_to_find, string):
        needwant_reviews.append(string)

print(needwant_reviews)
```
> ['sarah was able to help me find the items I needed quickly', 'great service from sara she found me what i wanted']

#### Removing punctuation from the strings (`[^w\s]`)  
`^` => not  
`\w` => word character
`\s` => whitespace character

```python
no_punct_reviews = []
pattern_to_find = r"[^\w\s]"

for string in customer_reviews:
    no_punct_string = re.sub(pattern_to_find, "", string)
    no_punct_reviews.append(no_punct_string)

print(no_punct_reviews)
```
> ['sam was a great help to me in the store', 'the cashier was very rude to me I think her name was eleanor', 'amazing work from sadeen', 'sarah was able to help me find the items I needed quickly', 'lucy is such a great addition to the team', 'great service from sara she found me what i wanted']

### Tokenization  
fundamental step in NLP involves converting our text into smaller units through a process  
individual words in the text become a `token`, but tokens can also be `sentences, subwords or individual characters`  

#### Importing NLTK
```python
import nltk
nltk.download('punkt_tab')
from nltk.tokenize import word_tokenize, sent_tokenize
```

#### Sentence Tokenization
```python
sentences = "Her cat's name is Luna. Her dog's name is Max"
sent_tokenize(sentences)
```
> ["Her cat's name is Luna.", "Her dog's name is Max"]

#### Word Tokenization
```python
sentence = "her cat's name is luna"
word_tokenize(sentence)
```
> ['her', 'cat', "'s", 'name', 'is', 'luna']

```python
sentence_2 = "Her cat's name is Luna and her dog's name is max"
word_tokenize(sentence_2)
```
> ['Her',
> 'cat',
> "'s",
> 'name',
> 'is',
> 'Luna',
> 'and',
> 'her',
> 'dog',
> "'s",
> 'name',
> 'is',
> 'max']  

### Stemming
standardize words by **reducing them** to their `root` or `base` form  
using `NLTK` package, we can utilize the `PorterStemmer` class for stemming words  

```python
from nltk.stem import PorterStemmer
ps = PorterStemmer()
```
> use `stem` method

```python
connect_tokens = ['connect', 'connected', 'connectivity', 'connect', 'connects']
for t in connect_tokens:
    print(t, ': ', ps.stem(t))
```
> connect :  connect  
> connected :  connect  
> connectivity :  connect  
> connect :  connect  
> connects :  connect  

```python
learn_tokens = ['learned', 'learning', 'learn', 'learns', 'learner', 'learners']
for t in learn_tokens:
    print(t, ": ", ps.stem(t))
```
> learned :  learn  
> learning :  learn  
> learn :  learn  
> learns :  learn  
> learner :  learner  
> learners :  learner  

```python
likes_tokens = ['likes', 'better', 'worse']
for t in likes_tokens:
    print(t, ": ", ps.stem(t))
```
> likes :  like  
> better :  better  
> worse :  wors  

### Lemmatization
stems the word to a *more meaningful base* form and ensure it does *not lose its meaning*  
using `NLTK` package, we can utilize the `WordNetLemmatizer` class for lemmatizing words

```python
nltk.download('wordnet')
from nltk.stem import WordNetLemmatizer
lemmatizer = WordNetLemmatizer()
```

```python
for t in connect_tokens:
    print(t, ': ', lemmatizer.lemmatize(t))
```
> connect :  connect  
> connected :  connected  
> connectivity :  connectivity  
> connect :  connect  
> connects :  connects  

```python`
for t in learn_tokens:
    print(t, ": ", lemmatizer.lemmatize(t))
```
> learned :  learned  
> learning :  learning  
> learn :  learn  
> learns :  learns  
> learner :  learner  
> learners :  learner  

```python
for t in likes_tokens:
    print(t, ": ", lemmatizer.lemmatize(t))
```
> likes :  like  
> better :  better  
> worse :  worse  

### N-grams
a sequence of neighboring `n` words or tokens, where `n` can be *any number*  
use `NLTK`, `Pandas` and `Matplotlib` to create and visualize n-grams

```python
import nltk
import pandas as pd
import matplotlib.pyplot as plt
```

```python
tokens = ['the', 'rise', 'of', 'artificial', 'intelligence', 'has', 'led', 'to', 'significant', 'advancements', 'in', 'natural', 'language', 'processing', 'computer', 'vision', 'and', 'other', 'fields', 'machine', 'learning', 'algorithms', 'are', 'becoming', 'more', 'sophisticated', 'enabling', 'computers', 'to', 'perform', 'complex', 'tasks', 'that', 'were', 'once', 'thought', 'to', 'be', 'the', 'exclusive', 'domain', 'of', 'humans', 'with', 'the', 'advent', 'of', 'deep', 'learning', 'neural', 'networks', 'have', 'become', 'even', 'more', 'powerful', 'capable', 'of', 'processing', 'vast', 'amounts', 'of', 'data', 'and', 'learning', 'from', 'it', 'in', 'ways', 'that', 'were', 'not', 'possible', 'before', 'as', 'a', 'result', 'ai', 'is', 'increasingly', 'being', 'used', 'in', 'a', 'wide', 'range', 'of', 'industries', 'from', 'healthcare', 'to', 'finance', 'to', 'transportation', 'and', 'its', 'impact', 'is', 'only', 'set', 'to', 'grow', 'in', 'the', 'years', 'to', 'come']
```

```python
unigrams = (pd.Series(nltk.ngrams(tokens, 1)).value_counts())
print(unigrams[:10])
```
> (to,)            7  
> (of,)            6  
> (the,)           4  
> (in,)            4  
> (and,)           3  
> (learning,)      3  
> (processing,)    2  
> (from,)          2  
> (is,)            2  
> (a,)             2  
> Name: count, dtype: int64  

```python
unigrams[:10].sort_values().plot.barh(color="lightsalmon", width=.9, figsize=(12,8))
plt.title("10 Most Frequently Occuring Unigrams")
```
> Text(0.5, 1.0, '10 Most Frequently Occuring Unigrams')  
![unigrams](/images/unigrams.png)  

```python
bigrams = (pd.Series(nltk.ngrams(tokens, 2)).value_counts())
print(bigrams[:10])
```
> (that, were)                   2  
> (rise, of)                     1  
> (of, artificial)               1  
> (artificial, intelligence)     1  
> (intelligence, has)            1  
> (has, led)                     1  
> (led, to)                      1  
> (to, significant)              1  
> (the, rise)                    1  
> (significant, advancements)    1  
> Name: count, dtype: int64  

```python
trigrams = (pd.Series(nltk.ngrams(tokens, 3)).value_counts())
print(trigrams[:10])
```
> (the, rise, of)                    1  
> (rise, of, artificial)             1  
> (of, artificial, intelligence)     1  
> (artificial, intelligence, has)    1  
> (intelligence, has, led)           1  
> (has, led, to)                     1  
> (led, to, significant)             1  
> (to, significant, advancements)    1  
> (significant, advancements, in)    1  
> (advancements, in, natural)        1  
> Name: count, dtype: int64  


