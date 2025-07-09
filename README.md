🎯 Sentiment Analysis on YouTube Comments
📌 Project Overview
This project presents a complete machine learning pipeline for performing sentiment analysis on YouTube comments. By leveraging both video metadata and user-generated text, the goal is to classify comments as positive or negative, providing actionable insights for content strategy, moderation, and user engagement.

🎯 Objectives
Classify YouTube comments into positive or negative sentiment.
Analyze correlations between sentiment and engagement metrics (likes, views, replies).
Evaluate multiple machine learning models using NLP techniques.
Generate business insights based on sentiment trends.
📁 Dataset Description
USvideos.csv: Video metadata (views, likes, dislikes, category, etc.)
UScomments.csv: User comments with likes and reply counts.
US_category_id.json: Mapping of category IDs to human-readable names.
🔄 Workflow Summary
1. Data Acquisition and Integration
Loaded video and comment datasets.
Mapped category_id to descriptive names.
Merged video metadata with comments using video_id.
2. Preprocessing
Cleaned comment text (punctuation, special characters, non-English words).
Applied lemmatization and tokenization.
Removed duplicates and handled missing values.
Labeled sentiment using VADER compound scores.
3. Exploratory Data Analysis (EDA)
Analyzed comment length distribution.
Created correlation heatmaps for engagement features.
Performed category-wise sentiment and activity analysis.
4. Feature Engineering
Generated engagement ratios.
Applied text vectorization using:
TF-IDF (unigrams and bigrams)
Bag of Words (CountVectorizer)
5. Model Building and Evaluation
Trained models using an 80/20 train-test split:

Model	Accuracy	F1 Score	ROC AUC	APS
Logistic Regression + TF-IDF (uni)	—	—	—	—
Logistic Regression + TF-IDF (bi)	—	—	—	—
Logistic Regression + BoW	95.7%	0.95	0.976	—
CatBoostClassifier	—	—	—	—
LGBMClassifier	—	—	—	—
DummyClassifier (baseline)	—	—	—	—
6. Inference on Unseen Comments
Final model generalized well to test data.
Predictions aligned closely with VADER sentiment scores.
💡 Business Insights & Recommendations
Entertainment and Music categories had the highest engagement and positive sentiment.
Comedy and News showed more polarized sentiment.
Sentiment is an independent signal not fully captured by views/likes and should be monitored directly for content strategy.
✅ Conclusion
This project demonstrates how sentiment analysis can be effectively applied to YouTube comments to uncover audience sentiment, guide content decisions, and improve platform engagement. The best-performing model, Logistic Regression with Bag of Words, achieved high accuracy and interpretability, making it suitable for real-world deployment.

BLANK_README.md to get started Build With: This is the list of the libraries used by me to run this project were pandas, numpy, matplotlib.pyplot, json, nltk, json, LabelEncoder, WordNetLemmatizer, TfidfVectorizer, stopwords, word_tokenize
re, string, spacy, train_test_split, classification_report, LogisticRegression,LGBMClassifier,nltk, SentimentIntensityAnalyzer,tqdm.
Getting Started: This is an example of how you may give instructions on setting up your project locally. To get a local copy up and running follow these simple steps. Prequisites: This is an example of software and how to install them. VS Code
How to Run
Clone this repository: https://github.com/sohini8328/Sentiment_Analysis_Youtube_Webiste.git

## Team
**Team Name:** Rate My Sentiments Engine

**Team Members:**
- Eric MacDougall
- Mark Luff
- Sohini Tomar
- Rawaa Yousseif 


