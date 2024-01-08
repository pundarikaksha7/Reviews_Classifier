# Reviews Classifier using Natural Language Processing (NLP)

Welcome to my NLP Project. This project will aim to classify Yelp Reviews into 1 star or 5 star categories based off the text content in the reviews.
We will use the Yelp Review Data Set from Kaggle.
Each observation in this dataset is a review of a particular business by a particular user.
The "stars" column is the number of stars (1 through 5) assigned by the reviewer to the business. (Higher stars is better.) In other words, it is the rating of the business by the person who wrote the review.
The "cool" column is the number of "cool" votes this review received from other Yelp users.
All reviews start with 0 "cool" votes, and there is no limit to how many "cool" votes a review can receive. In other words, it is a rating of the review itself, not a rating of the business.
The "useful" and "funny" columns are similar to the "cool" column.

# Structure of the report


1: Data exploration and analysis

2: Conversion of review texts into vectors using ```CountVectorizer``` class from ```sklearn.feature_extraction.text``` library.

3: Training a machine learning model. I used ```Naive - Bayes Classifier``` algorithm for the same due to its efficiency with text data.

4: Model evaluation.

5: Revaluation using text processing using ```Tfidf Transformer```.

6: Implementation using pipelines.

7: Model evaluation.

# Results

It was found that the model worked better without text processing using ```Tfidf Transformer``` due to the following reasons.

### Imbalanced Class Distribution:

Reviews with 1 star and 5 stars may have imbalanced distributions, meaning there might be significantly more reviews with one rating than the other. In such cases, the model may bias towards the majority class, making it challenging to accurately predict the minority class.

### Semantic Understanding 

TF-IDF focuses on the frequency of words but does not inherently capture the semantic meaning of words. Understanding sentiment often requires grasping the meaning of phrases and sentences, which might go beyond the capabilities of a simple TF-IDF model.

