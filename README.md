
# Topic modelling of user reviews
*Work in progress*

This Python application analyses more than 180k Google reviews of clothing shops in Berlin to extract topics of interest (staff friendliness, price, quality) and rate the stores in the different categories based on their contribution to the topics. Topic modelling is done with the top2vec package, a modern tool for topic extraction and semantic search (Angelov, 2020).

# Motivation
The main aim of this project is to automatically extract topics from customer reviews using state-of-the-art NLP techniques.

Customer reviews contain a variety of topics. For instance, reviews about clothing shops contain information about staff friendliness, price or product quality. Extracting these topics can help to pinpoint the user needs and to provide recommendations for new users depending on their specific interests. In this sense, a user interested in social aspects of the purchase experience might go for shops with a high score in staff friendliness, whereas clients interested in monetary aspects might value price over any other aspect.

## Final procuct
The final expected product is an application hosted in Streamlit in which the user can choose a neighborhood and a type of shop to get a map of shops complying with the criteria. The user is able to select a shop to see its ratings in the 3 topics of interest (staff friendliness, price and quality).

## Technical overwiew
This project uses NLP tools in Python (top2vec, BERT, BERTopic) to explore the topics of over 180k Google reviews of clothing shops in Berlin.

## Current work
The reviews will be split in training (reviews before 2022) and test data (reviews in 2022). I will use the predicted probabilities to predict the 3 top topics for each document of the 2022 reviews (unseen, test data).

After topic modelling, the shops will be assigned a probability in the different topics, based on their mean score in the relevant topic.


Angelov, D. (2020). Top2vec: Distributed representations of topics. arXiv preprint arXiv:2008.09470.
