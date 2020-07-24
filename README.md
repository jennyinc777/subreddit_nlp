# Natural Language Processing for Question & Answer Websites

## Problem Statement

1.  We want to build a robust model for our question-and-answer website that can categorize advice columns and explanatory forums based on the language of Reddit’s two subreddits:  r/advice and r/explainlikeimfive.

2.  Figure out what language differentiates these two subreddits

## Executive Summary

Using industry standard machine learning algorithms, we take a whopping 10,000 recent hot posts from r/advice and r/explainlikeimfive to train our model to be able to differentiate between the two subreddits.  We use some lemmatizing algorithms along with two vectorizers to find common and popular words.

We have done a lot of data processing in the past such as wrangling in [standardized testing scores](https://git.generalassemb.ly/jennyinc777/project_1) to understand why some states have high participation rates while some have low particpation rates in the U.S.  We've also worked with prediction machine learning algorthms, particiularly with linear regression statistical modeling, when dealing with the [Ames housing dataset](https://git.generalassemb.ly/jennyinc777/project_2/tree/working).  And we're eager to tackle yet another form of prediction analysis and have been using categorical models in house.

We are proposing looking at quite of few options to tackle building a robust model.  This includes using both a `CountVectorizer` and a `TfidfVectorizer` to assist with stop words as well as using a `PorterStemmer` to find the lemma to similar words.  Next, the estimators that we will use include the tried-and-true `LogisticRegression` along with `MultiNomial Naive Bayes`.  Moving into ensemble methods, we will be fitting data to a `BaggingClassifier`, `RandomForestClassifier`, and `AdaBoost`.  We will also be exploring how much data to add.  With something like Reddit, we have the decision to pull in the title, the description text, as well as any comments.  Ultimately, we will be looking for a model that delivers on time and accuracy and we're excited to work with this data to help solve your business problem.

We are meticulous, detail-oriented, and will turn this problem on its head to find the best solution for you.  We won't stop at just one or two models; we will provide a comprehensive solution that really helps propel your question-and-answer website's efficiency to better assist the users on your site.  Look forward to work with you.

## What is in this repo?

| Folder/File | Description |
|-|-|
| data | advice.csv, eli5.csv, both_subreddits.csv are files that are saved when running the Jupyter notebooks in this repository. |
| assets | images used in the Jupyter notebooks as Markdown |
| `EDA.ipynb` | exploratory data analysis notebook |
| `Extract_n_Load.ipynb` | extracting data from Reddit |
| `Graphs.ipynb` | presentation graphs |
| `Modeling1.ipynb` | models include logistic regression and multinomial naive bayes |
| `Modeling2.ipynb` | models include bagging classifier, random forest classifier, and adaboost |
| `NLP.pptx` | presentation deck that give a brief overview and some recommendations  |
| `requirements.txt` | requirements to run the files in this repo |

## Data Dictionary

| Columns | Description |
|-|-|
| author | author of the Reddit post |
| created_utc | this column is in Unix/Epoch time |
| selftext | description of the Reddit post |
| subreddit | r/explainlikeimfive or r/advice |
| title | title of the Reddit post |

## Conclusion/Recommendations

- Our model with the best test score of 0.9892 includes a `CountVectorizer` with a `PorterStemmer` as the analyzer and a `LogisticRegression()` classifier.
- To make a robust model, it is highly recommended that the company use a Porter Stemmer or some sort of lemmatizing device.
- Logistic regression and Multinomial Naive Bayes yielded better results with smaller amounts of information.
- With “self text” column pulled in, Random Forest, Boosting, and Bagging seemed to work well.
- The two subreddits shared a few common words (e.g. feel, like).  However, the advice subreddit had more words pertaining to advice (e.g. don’t, know, need, help).

Please look through Modeling1.ipynb and Modeling2.ipynb to get a better understanding of model scores.
