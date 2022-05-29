# FakeNews Classification 
This is ML students repository from C22-PS051 Team doing capstone Bangkit 2022. For MD repository [click here](https://github.com/FakeNews-Detector/FakeNews-App). 

# Prerequisite

In this project we are going to creat a model for Fake news Classification. So we need to install some libraries as follows:
1. Pandas
2. Numpy
3. Matplotlib
4. NLTK
5. Scikit-learn
6. Sastrawi
7. Beautiful Soup
8. Regex
9. Requests
10. Tensorflow


# Activities

## First Week

We were looking for the dataset needed to build a fake news classification model. However, many datasets were not what we wanted. So we're looking for valid and hoax news data on some websites.

For valid news data, we obtained from [Indonesian News Corpus](https://data.mendeley.com/datasets/2zpbjs22k3/1) around 150k of json & XML files collected by some researchers. As for the hoax news we've obtained from the website [TurnBackHoax](https://turnbackhoax.id/) using web scrapping with data around 90k.

After successfully compiling the data, we limit the data that will be used as much as 3 columns (title columns, links, and categories) so as to allow for the preprocessing data. Then we combine the two data into one and label the data with a label 1 for valid news and a label 0 for the hoax news. We categorized the label from the source of website (some research called it clustering). 

## Second Week

After successfully collecting data and creating our own dataset, we began the data preprocessing. We do the preprocessing data with the 4 step as follows:
1. Data cleaning

Data cleaning is the process to clean data such as remove punctuation, lowering text, remove number, and remove whitespace

2. Stemming

Stemming is the process of reducing a word to its word stem that affixes to suffixes and prefixes or to the roots of words known. We are using [Sastrawi Stemmer](
https://pypi.org/project/Sastrawi) for stemming


3. Stopwords removal

Stopwords are actually the most common words in any language (like articles, prepositions, pronouns, conjunctions, etc) and does not add much information to the text. So we did the stopwords removal in Indonesian Language. 

4. Tokenizing

Tokenizing is the process to break the text into smaller units called tokens. Tokens can be a sentence or word. In this data, we want to tokenize text into word. 

