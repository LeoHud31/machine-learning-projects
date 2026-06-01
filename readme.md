# ***Machine Learning Projects***
In this repositiory I have examples of projects that I have done. These will manily focus around Natural Language Processing and argument mining, but not exclusively. 

# ***Restaurant Reviews***

This repository contains a Jupyter Notebook demonstrating a simple NLP sentiment classification workflow applied to a restaurant reviews dataset. The notebook trains a TF-IDF with an SGDClassifier pipeline and includes evaluation and visualizations.

## What the project does

Takes a pre-prepared dataset of restaurant reviews "Resaurant reviews, dataset for Natural language processing by Arsh Anwar on Kaggle". Which are labeled as either positive or negative and will try and predict whether a review is positive or negative. 

## What I used and learnt

- Tokenisation with NLTK
- NLP models and pipelines
- Various resuseable code in future such as balanced accuracy and confusion matrix

## Key files

- Notebook: [restaurant_reviews/restaurant_review.ipynb](restaurant_reviews/restaurant_review.ipynb)
- Dataset: [restaurant_reviews/Restaurant_Reviews.tsv](restaurant_reviews/Restaurant_Reviews.tsv)

## Evaluation & expected results

- I have achieved currently around 0.846 (84.6%) with the current setup (1,000 reviews, 800 train samples and 200 test samples). 

# ***YouTube Comments***
This section of the repository is a series of notebooks created around the dataset "Youtube Comments Data - Doctor Mike VS 20 Anti-Vaxxers | Surrounded - Jubilee by Manjit Baishya on Kaggle".

# ***Toxic YouTube Comments Classification***
The first notebook in this collection is "youtube_comments_toxic_classification.ipynb" 
This first counts the amount of emojis that are used in comments and how many comments contain one. 
It then uses NLTK to classify the sentiment of the comments into positive, neutral and negative. 
Using this it then clasifies the toxicity of the negative comments to create a hate model and a new dataset with the hate classification. 

## What I used and learnt

- detect emojis in text
- NLTK sentiment analysis
- Pytorch text classification

## Key files

- Notebook: [youtube_comments/youtube_comments_toxic_classification.ipynb](youtube_comments/youtube_comments_toxic_classification.ipynb)
- input dataset: [youtube_comments/comments.csv](youtube_comments/comments.csv)
- output dataset: [youtube_comments/negative_comments_with_labels.csv](youtube_comments/negative_comments_with_labels.csv)

# ***Positive YouTube Comments Classification - Toxic comments inverse***
The first notebook in this collection is "youtube_comments_positive_classification.ipynb"  
It then uses NLTK to classify the sentiment of the comments into positive, neutral and negative. 
Using this it then clasifies the positive comments to create a positive model and a new dataset with the positive classification. 

## What I used and learnt

- NLTK sentiment analysis
- Pytorch text classification

## Key files

- Notebook: [youtube_comments/youtube_comments_positive_classification.ipynb](youtube_comments/youtube_comments_positive_classification.ipynb)
- input dataset: [youtube_comments/comments.csv](youtube_comments/comments.csv)
- output dataset: [youtube_comments/positive_comments_with_labels.csv](youtube_comments/positive_comments_with_labels.csv)

# ***YouTube Comments Argument Mining***
This notebook is the argument mining of the main dataset. It takes in the 2 datasets made previously runs some reasoning and stance detection and outputs the stance based on the argument. It then creates and trains a model to predict the stance with a 98.58% accuracy.


## What I used and learnt
- Argument mining
- sentiment analysis
- NLP
- GPU processing

## Key files
- Notebook: [youtube_comments/youtube_comments_argument_mining.ipynb](youtube_comments/youtube_comments_argument_mining.ipynb)
- Input dataset: [youtube_comments/negative_comments_with_labels.csv](youtube_comments/negative_comments_with_labels.csv)
- Input dataset: [youtube_comments/positive_comments_with_labels.csv](youtube_comments/positive_comments_with_labels.csv)
- output dataset: [youtube_comments/youtube_comments_argument_mined.csv](youtube_comments/youtube_comments_argument_mined.csv)
- output dataset: [youtube_comments/youtube_comments_with_predictions.csv](youtube_comments/youtube_comments_with_predictions.csv)
- output model: [youtube_comments/AM_models/best_stance_model.joblib](youtube_comments/AM_models/best_stance_model.joblib)
- output model: [youtube_comments/AM_models/stance_lr_model.joblib](youtube_comments/AM_models/stance_lr_model.joblib)
- output model: [youtube_comments/AM_models/tfidf_vectorizer.joblib](youtube_comments/AM_models/tfidf_vectorizer.joblib)