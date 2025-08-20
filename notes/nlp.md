
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