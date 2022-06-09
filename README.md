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

After that we split the data into training data and validation data. For training data, you can look up to data/fake_train.xlsx and real_train.xlsx which is contain 13.422 data. Then for validation data, you can look up to data/fake_testing.xlsx and real_testing.xlsx which is contain 3354 data. Last but not least for testing data, we download it from [kaggle](https://www.kaggle.com/datasets/muhammadghazimuharam/indonesiafalsenews). You can look up to data/Data_latih.csv which is contain 4231 data. 

## Third Week
After that, we were trying to build model using LSTM and tuning the hyperparameters. In this model, the training accuracy reach 93%, the validation accuracy reach 80% and the testing accuracy reach 74% which is not good enough. You can look up the model we have done in /src/lstm_model.h5 and lstm_weights.h5.

## Fourth Week
After finishing build a model. We are trying to evaluate and test for model prediction on a new data / text. You can look up for our data testing on /data/Data_uji.csv. We got some error for testing the valid news because we trained outdated news. But it did well on Hoax News. 


