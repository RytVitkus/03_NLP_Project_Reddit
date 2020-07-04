# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP


### Introduction

The aim of this project was to gather data from two subreddits of my choosing using Pushshift’s Reddit API, and create a model that could predict what subreddit a post came from. In this project I grabbed 7000 posts from r/WoT (Wheel of Time subreddit, dedicated to the 15 books series by Robert Jordan & finished by Brandon Sanderson) and 6000 posts from r/asoiaf. (A Song of Ice and Fire subreddit, strictly dedicated to the books by George R. R. Martin. TV discussion is dissuaded for other related subreddits)


### EDA 

- I had to grab 13000 posts in total, with more from WoT. This was due to there being more empty values in the WoT subreddit than asoiaf. (Usually the result of moderators removing a post, or the original poster removing the post)
- Following cleaning (dropping nulls, removing duplicates) I had a nearly even split of data, with slightly more posts from Asoiaf.
- 4,980 posts from r/WoT & 5108 posts from r/asoiaf



---

### Conclusion / Model Performances

Models were evaluated using accuracy as the metric. Baseline accuracy was ~51%


- **Best** CountVectorizer Transformer / Logistic Regression Classifier:
- Train: 0.9894, Test: 0.9874
- TFIDF Transformer / Logistic Regression Classifier
- Train: 0.979, Test: 0.9815
- CountVectorizer Transformer / $k$-NN Classifier:
- Train: 0.5981, Test: 0.6211
- TFIDF Transformer / $k$-NN Classifier:
- Train: 0.5111, Test: 0.5137
- CountVectorizer Transformer/ Multinomial Naive Bayes Classification:
- Train: 0.9786, Test: 0.9765

Overall, my Logistic regression peformed the best. With tuning, removing additional words, adjusting  hyperparameters. My next steps at this stage are to investigate the posts my model got wrong and see if it's just certain words missing, or if they're removed posts. 



---

#### Slides

https://docs.google.com/presentation/d/1qE814MkzvC8-ajry7dyTJA5j_0NVWn1mM_aa1cKIt2Q/edit?usp=sharing


