# NLP-Comedy_routines

Tools used:
Python - gensim, nltk, BeautifulSoup, TextBlob, WordCloud

# Quick Summary

● Web-scraped 12 transcripts from websites using BeautifulSoup module in python

● Cleaned and organized the data into two different formats; corpus, document-term matrix

● Analyzed the sentiments using polarity and subjectivity metrics and achieved feedback rating of 84% from the public

● Identified topics in routines lasting 30 minutes using the topic modeling technique, Latent Dirichlet Allocation

● Experimented with Bayesian techniques to generate comedy transcripts similar to the ones given as input the Bayesian model

# DETAILS ABOUT THE PROJECT:

# Data Cleaning
## Introduction
This notebook goes through a necessary step of any data science project - data cleaning. Data cleaning is a time consuming and unenjoyable task, yet it's a very important one. Keep in mind, "garbage in, garbage out". Feeding dirty data into a model will give us results that are meaningless.

Specifically, we'll be walking through:

Getting the data - in this case, we'll be scraping data from a website
Cleaning the data - we will walk through popular text pre-processing techniques
Organizing the data - we will organize the cleaned data into a way that is easy to input into other algorithms
The output of this notebook will be clean, organized data in two standard text formats:

Corpus - a collection of text
Document-Term Matrix - word counts in matrix format
Problem Statement
As a reminder, our goal is to look at transcripts of various comedians and note their similarities and differences. Specifically, I'd like to know if Ali Wong's comedy style is different than other comedians, since she's the comedian that got me interested in stand up comedy.


When dealing with numerical data, data cleaning often involves removing null values and duplicate data, dealing with outliers, etc. With text data, there are some common data cleaning techniques, which are also known as text pre-processing techniques.

With text data, this cleaning process can go on forever. There's always an exception to every cleaning step. So, we're going to follow the MVP (minimum viable product) approach - start simple and iterate. Here are a bunch of things you can do to clean your data. We're going to execute just the common cleaning steps here and the rest can be done at a later point to improve our results.

## Common data cleaning steps on all text:

Make text all lower case

Remove punctuation

Remove numerical values

Remove common non-sensical text (/n)

Tokenize text

Remove stop words

## More data cleaning steps after tokenization:

Stemming / lemmatization

Parts of speech tagging

Create bi-grams or tri-grams

Deal with typos




# Getting The Data
Luckily, there are wonderful people online that keep track of stand up routine transcripts. Scraps From The Loft makes them available for non-profit and educational purposes.

To decide which comedians to look into, I went on IMDB and looked specifically at comedy specials that were released in the past 5 years. To narrow it down further, I looked only at those with greater than a 7.5/10 rating and more than 2000 votes. If a comedian had multiple specials that fit those requirements, I would pick the most highly rated one. I ended up with a dozen comedy specials.


# Exploratory Data Analysis:

Performed a few EDA tasks on the dataset to learn a few things about each comedian and also plotted a few graphs like the ones below to find patterns in their routines;

![image](https://user-images.githubusercontent.com/64389100/138031130-0505a36d-ac72-469b-8765-3d83d8d39615.png)

![image](https://user-images.githubusercontent.com/64389100/138031242-d549c963-acea-4471-8c63-5071b0205acd.png)


# Sentiment Analysis

Analyzed the sentiments of each comedian. Used Subjectivity and Polarity metrics to understand their sentiments and also plotted the speech-positivity graphs for each comedian to know their change of the sentiments during a performance


![image](https://user-images.githubusercontent.com/64389100/138031622-dbdf851f-99a2-4c6b-90d4-6baa228f1e9e.png)


![image](https://user-images.githubusercontent.com/64389100/138031848-aa078206-767d-49c4-a2b1-bba698681cd7.png)

      Analysis of positivity flow of a routine


