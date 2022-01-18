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
My training and testing score stayed in the 90s. When choosing these subreddits I expected a lot of overlap because they both seemed very similar but after running these models it’s clear that they had no problem differentiating the two. The list of top words for either were different enough for the most part, it seems that the users of these subreddits were both looking for answers for their questions but the types of questions asked differed enough to produce a fairly accurate model.