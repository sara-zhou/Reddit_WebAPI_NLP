# Project 3: Natural Language Processing on Reddit

## Problem Statement

Given a post from either r/OutOfTheLoop and r/explainlikeimfive, how well can we predict which subreddit it came from?

#### Background

NLP(Natural Language Processing) converts humans language into computer-readable data that can be analyzed and fit to various statistical models. The application of this technology ranges from translation services (i.e. Google Translate) to artificial intelligence. For our purposes, we're going to pull a large set of posts from either subreddit using the PushShift API and perform analysis on a selection of recent usable posts to predict which subreddit it originates from.


### Datasets

* [`ootl_posts.csv`](./data/ootl_posts.csv): Posts from r/OutOfTheLoop
* [`elif_posts.csv`](./data/elif_posts.csv): Posts from r/explainlikeimfive


### Data Dictionary

|Feature|Value|
|---|---|
|**subreddit**|the subreddit in which the post originates from|
|**title**|title of the reddit post|
|**selftext**|the body text of the post|
|**created_utc**|time that the user posted the post|

---

## Conclusions
Despite my initial ideas that certain words or phrases would be more common in either subreddit, I did not find any evidence of such. Regardless of pretty much any type of model that I did, my training and testing score sat right around 75%. Even in adjusting my grid search parameters and taking subsamples of the data, there appears to be somewhat of a cap on how good a model can be for these particular two subreddits.
My thinking to explain this is that there is a lot of overlap between either subreddit. The list of top words for either were nearly identical and, for the most part, it seems that the users of these subreddits are looking for holiday advice. Whether or not they wanted to travel with others didn't seem to affect this. I did find it interesting that some very different models (for example, Multinomial Naïve Bayes and Adaboost Classifier) produced nearly the same results. I unfortunately don't have a scientifically backed explanation for why this may be, but nevertheless, we were still able to correctly predict the subreddit roughly 3 out of every 4 times. Not the greatest, but not the worst.