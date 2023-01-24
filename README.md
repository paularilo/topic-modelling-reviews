# Topic modelling of user reviews

This Python application analyses more than 180k Google reviews of clothing shops in Berlin to extract topics of interest (staff friendliness, price, quality) and rate the stores in the different categories based on their contribution to the topics. Topic modelling is done with the top2vec package, a modern tool for topic extraction and semantic search (Angelov, 2020).

## MOTIVATION
The main aim of this project is to automatically extract topics from customer reviews using state-of-the-art NLP techniques.

Customer reviews contain a variety of topics. For instance, reviews about clothing shops contain information about staff friendliness, price or product quality. Extracting these topics can help to pinpoint the user needs and to provide recommendations for new users depending on their specific interests. In this sense, a user interested in social aspects of the purchase experience might go for shops with a high score in staff friendliness, whereas clients interested in monetary aspects might value price over any other aspect.

## TECHNICAL OVERVIEW
This project uses Python and top2vec to model the topics of over 180k Google reviews of clothing shops in Berlin.

The Google reviews were split in training (reviews before 2022) and test data (reviews in 2022). In the machine learning part, we used latent dirichlet allocation (LDA) and BERTopic to model the topics contained in the training data set. We then used BERTopic model to get predicted probabilities, where the probabilities of a review belonging to each topic are computed. Finally, we used the trained BERTopic model to predict the 3 top topics of the 2022 reviews (unseen, test data).

After topic modelling, the shops were assigned a score in the different topics, based on score in the relevant topic.

## FINAL PRODUCT
The final product is an application hosted in Streamlit in which the user can choose a neighborhood and a type of shop, where the product provides different textual and graphical information.


Angelov, D. (2020). Top2vec: Distributed representations of topics. arXiv preprint arXiv:2008.09470.
