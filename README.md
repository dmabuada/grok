# Introduction

Grok /ˈɡrɒk/ is a term that roughly means "to understand profoundly/have knowledge of". It was coined by Robert Heinlein in his science-fiction novel *Stranger in a Strange Land*.

Grok uses sentiment analysis techniques to characterize the sentiment of text units. In this case, Grok parses through NYmag's article content and expresses articles as having positive, negative, or neutral sentiment. It then matches them against article pageviews, e.g. "Article 2007/07/the_entourage_guiltpleasure_in_3.html has 100 pageviews and rates as 90% positive".

# Installation

First ensure that Python 3.0 or later is installed. Build the required docs in your local (virtual!) env, from the project directory:

```
virtualenv -p python3 envname
source envname/bin/activate
pip install -r requirements.txt
```

Since Matplotlib is being used to plot the graphs, a backend must be specified:

```
echo "backend: TkAgg" >> ~/.matplotlib/matplotlibrc
```

# Generate OAuth Credentials

Grok requires OAuth credentials in order to generate Google Analytics data. See [here](https://developers.google.com/api-client-library/python/guide/aaa_client_secrets) about generating a client_secrets.json file.

# Running Grok

```
python manage.py runserver
```


