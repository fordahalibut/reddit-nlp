# Natural Language Processing - A Reddit study
## Problem
With approximately 14,000 reddit post titles and accompanying text, can we use natural language processing to build a classification model that will accurately predict whether the post was made by a bot?
## Executive Summary
- Logistic Regression performed the best, achieving 98% accuracy on training data and 94% accuracy on unseen data.
- The final parameters used Lasso Regularization with a regularization strength of 0.5
- Vectorization was achieved using CountVectorizer with RegEx tokenization.

The very high accuracy of the model implies that we can quite easily distinguish between these two subreddits using only bag of words methods. Upon reflection, perhaps `AskReddit` isn't as good of a stand-in for a general topic forum as hoped. 

Given more time, I would instead take a sampling of each individual subreddit that `SubredditSimulator` pulls from, to get a more equivalent corpus of words.
## Contents
1. [Importing Libraries](#1.-Importing-libraries)
2. [Function to scrape current reddit data through the API](#2.-Function-to-scrape-current-reddit-data-through-the-API)
3. [Function to scrape historical data](#3.-Function-to-scrape-historical-data)
4. [Gathering data](#4.-Gathering-data)
5. [EDA and clean up](#5.-EDA-and-clean-up)
6. [Model selection and evaluation](#6.-Model-selection-and-evaluation)
7. [Feature correlations](#7.-Feature-correlations)
8. [Word Cloud representations using Tableau](#8.-Word-Cloud-representations-using-Tableau)
9. [Investigating occurence of common stop words in each subreddit](#9.-Investigating-occurence-of-common-stop-words-in-each-subreddit)
10. [Conclusion](#10.-Conclusion)

## Data
Sources: 
- [SubredditSimulator](https://www.reddit.com/r/SubredditSimulator)
- [AskReddit](https://www.reddit.com/r/AskReddit)
- [Pushshift.io API](https://github.com/pushshift/api)

### 10. Conclusion

The very high accuracy of a logistic regression model implies that we can quite easily distinguish between these two subreddits using only bag of words methods. Upon reflection, perhaps `AskReddit` isn't as good of a stand-in for a general topic forum as hoped. 

Given more time, I would instead take a sampling of each individual subreddit that `SubredditSimulator` pulls from, to get a more equivalent corpus of words.
