# Sentiment_Analysis_Youtube_Webiste
Sentiment Analysis on Youtube website
Sentiment Analysis of YouTube Comments
Project Overview
This project presents a complete machine learning pipeline to perform sentiment analysis on YouTube comments. Using both video metadata and textual user comments, the objective is to build a model that classifies comments as positive or negative. The outcome can be used to inform content strategy, improve moderation, and enhance user engagement on video platforms.

Objectives
Classify YouTube comments into positive or negative sentiment.
Analyze correlations between sentiment and engagement metrics (likes, views, replies).
Evaluate multiple machine learning models using NLP feature extraction techniques.
Generate insights and business recommendations based on sentiment patterns.
Dataset Description
USvideos.csv: Video metadata including views, likes, dislikes, category, and more.
UScomments.csv: User-generated comments with likes and reply counts.
US_category_id.json: Mapping of category IDs to human-readable names.
Workflow Summary
1. Data Acquisition and Integration
Loaded video and comment datasets.
Mapped category_id to descriptive category names.
Merged video metadata with user comments using video_id.
2. Preprocessing
Cleaned comment text (punctuation, special characters, non-English words).
Applied lemmatization and tokenization.
Removed duplicates and handled missing data.
Labeled sentiment using VADER compound scores.
3. Exploratory Data Analysis (EDA)
Distribution of comment lengths.
Correlation heatmap of engagement features.
Category-wise sentiment and activity analysis.
4. Feature Engineering
Generated engagement ratios.
Text vectorization using:
TF-IDF (unigrams and bigrams)
Bag of Words (CountVectorizer)
5. Model Building and Evaluation
Trained models using an 80/20 train-test split:

Logistic Regression + TF-IDF (unigrams)
Logistic Regression + TF-IDF (bigrams)
Logistic Regression + BoW
CatBoostClassifier
LGBMClassifier
DummyClassifier (baseline)
Evaluation metrics:

Accuracy
F1 Score
ROC AUC
Average Precision Score (APS)
Best Performing Model:

Logistic Regression + Bag of Words
Accuracy: 95.7%
F1 Score: 0.95
ROC AUC: 0.976
6. Inference on Unseen Comments
Final model successfully generalized to test data.
Predictions aligned well with VADER sentiment scores.
7. Business Insights & Recommendations
Entertainment and Music categories had the highest engagement and positive sentiment.
Comedy and News had more polarizing sentiments.
Sentiment is an independent signal not fully captured by views/likes, and should be monitored directly.
How to Run
Clone this repository:
git clone 
cd Youtube-Sentiment-Analysis

## Team
**Team Name:** Rate My Sentiments Engine

**Team Members:**
- Eric MacDougall
- Mark Luff
- Sohini Tomar
- Rawaa Yousseif 


