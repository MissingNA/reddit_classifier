# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP
#### Eu Jin Lee: [GitHub](https://github.com/missingNA)

## Problem Statement

As part of a data science team working with the National Suicide Prevention Lifeline, our aim is to monitor the activities of users of certain subreddits for any posts that suggest self harm and be able to notify our response teams accordingly. Why Reddit? We recognize that Reddit is a popular digital safe space for the younger generation to express themselves, their concerns and obtain life changing advice. Paired with the fact that there has been an uptick of mental health issues that are affecting our youth today. 

In this project, we focused on working with classifier models, including Logistic Regression, Naive Bayes and Support Vector Machines (SVM), and natural language processing techniques such as pulling text off the web with APIs, parsing text with tokenizers and regex expressions, vectorizing text into features that can be trained on with classifiers to draw conclusions.

## Executive Summary
The workflow of the projects is as follows:
    - Importing packages, data scraping, cleaning and combining datasets
    - Exploratory data analysis to identify any insights to the nature of the data statistics
    - Modeling 
    - Model Selection 
    - Model Evaluation
    - Conclusions and Recommendations
    
For the purposes of this project, we pulled from the subreddits r/SuicideWatch and r/OffMyChest. These are moderately large volume subreddits, the purpose of which is to allow redditors a safe space and to make themselves feel heard. What we realized is that the these posts range from expressing intent of hurting themselves, personal anecdotes and providing advice. These posts may contain very insightful information into the lives of the people battling with depression and mental health issues, potentially giving us answers to the underlying psychological triggers from a person's history or current overall environment. 

### Datasets
Dataset used for the project can be found:
[here](https://git.generalassemb.ly/ejlee/project_3/blob/master/posts_final.csv)

#### Data Dictionary 
For this project, the data dictionary for posts_final.csv:
| Features     | Type   | Description                                           |
|--------------|--------|-------------------------------------------------------|
| id           | object | the unique identification key for each post           |
| title        | object | the title of the subreddit post                       |
| selftext     | object | the content of the subreddit post                     |
| subreddit    | object | the respective subreddit the post belongs to          |
| created_utc  | int64  | the epoch time of post creation                       |
| author       | object | Redditor username                                     |
| score        | int64  | the respective score of the post determining its rank |
| num_comments | int64  | the number of comments per post                       |
| word_length  | int64  | the word length of the post                           |

---
## Conclusion and Recommendations 

Based on our final model, which performed with a 83.5% accuracy in predicting the correct subreddit. This is useful for us to reclassify the subreddits we were monitoring to resume operations after the recent power outage that corrupted the data files we have collected.

More importantly, we can dive deeper into the word frequencies, develop narratives and theories that help to explain the mental and social challenges that this generations faces today and find ways to tackle these issues. We will continue to develop our model, possibly feature engineering a triage system that helps rank the severity of harming intent and help these most in need first. 

## References

-Normalizing the Conversation:
- https://www.spsnational.org/the-sps-observer/fall/2018/mental-health-mattersnormalizing-conversation

SVM and Naive Bayes models for NLP:
- https://medium.com/@bedigunjit/simple-guide-to-text-classification-nlp-using-svm-and-naive-bayes-with-python-421db3a72d34

NLP Workflows:
- https://medium.com/@ageitgey/natural-language-processing-is-fun-9a0bff37854e