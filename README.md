# JeroenPortfolio
Summary of all projects


# [Project 1: Recommender systems]( https://github.com/JeroenSimonse/ThesisProject )

This project was part of my thesis: 'Comparing collaborative filtering with content based filtering on Steam games', and marked my last project before graduating.
The main goal of the project was constructing both a collaborative and content based recommendersystem, to compare the performance of both of these techniques. 
In short, the project can be devided in the following tasks:
1. Cleaning the Steam user dataset
2. Cleaning the Games dataset
3. Creating a User-Item interaction matrix
	* This matrix represents all interacted items per user
4. Constructing the two recommendersystems 
	* Collaborative filtering / Content based filtering
5. Evaluating both models

## Collaborative Filtering

There are several ways to construct a collaborative filtering (CF) model, but the most conventional model is a Singular Value Decomposition(SVD) model. 
For this project, SVD was also used to construct the CF model.
SVD first decomposes the User-Item matrix, and then reconstructs it by calculating the dot product between the decomposed matrices. 
The reconstructed matrix contains the recommendations for all users.

## Content based Filtering

Content based filtering (CBF) focusses more on the contents of the items, in this case the games. 
It recommends games to users that are similar to the games the user already played, based on its contents. 
For this method the first step is to create user profiles for all users and item profiles for all items. 
After these profiles are built, they can be vectorized by a simple vectorizer. 
The last step is to calculate the similarities between the profiles based on the cosine similarity. 
The most similar items get recommended to the user. 

## Results

# [Project 2: Sentence classification]( https://github.com/JeroenSimonse/DeepLearningProject )
This project was part of our Deep Learning course and consisted of the following tasks:
1. Text classification
	* Is a sentence original English or translated from French to English by using a Neural Network model
2. Format the predictions in a text file 

The model that was constructed for this project, was a Bidirectional LSTM Recurrent Neural Network, with the following architecture:

![](/images/Model%20architecture.png)

## Results
The model was optimized with the adam algorithm and got to an accuracy of 75,5%.

![](/images/Model%20accuracy%20DL.png)






