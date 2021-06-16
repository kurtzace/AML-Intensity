## Goal
to compute intensity of AML words per company

Imagine you web search a company and you wish to count the number of times blacklist,sanction,ofac,embargo 
appeared - irrespective of their variations like pluralized (blacklists), superlative form, or variations (ban/restrictions). 

This mini pipeline could assist you. 

On a high level it does the following
- Gets bing search result of a company
- Removes proper nouns/companies/people
- remove stopwords like a, an, um
- remove punctuation
- lemmatize best, better to equivalent words like good
- searches and increments counts for similar words

## Input output example
Input: EMARAT KAVKAZ
Output: {'blacklist': 24, 'sanction': 12, 'ofac': 0, 'embargo': 11}

## Tech used
- NLTK
    > Stopwords
    > Tokenization
    > Part of speech tagging
- Textblob
- Gensim with google negative wordtovec text embeddings pretrained model


## setup
```
python -m venv nlp
cd nlp
cd Scripts
activate
CD ../..
cd NLP
mkdir AmlIntensity
cd AmlIntensity
pip install nltk
pip install textblob
pip install requests
pip install gensim
pip install scikit-learn
pip install notebook
```