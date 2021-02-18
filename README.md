# Profile 
* Name: Jeroen Simonse
* Age: 24
* Sex: Male
* Education: Master of Science (Msc) in Data Science and Society
* Skills: Python, R, Machine Learning, Deep Learning, MS Office
* Interests: Tech enthousiast, Working out, Skiing, Friends



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

![](/images/cfmodel.png)

## Content based Filtering

Content based filtering (CBF) focusses more on the contents of the items, in this case the games. 
It recommends games to users that are similar to the games the user already played, based on its contents. 
For this method the first step is to create user profiles for all users and item profiles for all items. 
After these profiles are built, they can be vectorized by a simple vectorizer. 
The last step is to calculate the similarities between the profiles based on the cosine similarity. 
The most similar items get recommended to the user. 

![](/images/cbmodel.png)

## Results

The collaborative filtering model was performing better compared to the content based model. More specifically, the model with seven latent factors and smooted ratings performed best.



# [Project 2: Sentence classification]( https://github.com/JeroenSimonse/DeepLearningProject )
This project was part of our Deep Learning course and consisted of the following tasks:
1. Text classification
	* Is a sentence original English or translated from French to English by using a Neural Network model
2. Format the predictions in a text file 

The model that was constructed for this project, was a Bidirectional LSTM Recurrent Neural Network, with the following architecture:

![](/images/modelarchitecture.png)

## Results
The model was optimized with the adam algorithm and got to an accuracy of 75,5%.

![](/images/modelaccuracydl.png)


# [Project 3: Multi-linear regression inferential modeling/predictive modeling]( https://github.com/JeroenSimonse/StatisticsProject ) 

This project was made for our Statistics course and consisted of the following goals:
1. Data preparation
	* Evaluate the extent of the missing data
	* Treat univariate outliers
	* Treat multivariat outliers
	* Treat missing data
2. Inferential modeling task
	* Make a selection of all relevant features
	* Using MLR to asses if conservative attitudes are good or bad for your psychological well-being
3. Predictive modeling task
	* Make a selection of all relevant features
	* Using MLR to predict how satisfied people are with life

Based on the dataset *Wave 6 of the World Values Survey*.


## Results  
For the inferential modeling task, conservatism had a significant positive effect on the psychological well-being of people, after controlling for confounding variables.
With the predictive modeling taske, the model managed to predict satisfaction with life with a RSME of 1.38  on a scale of 0-10.


# [Project 4: Image classification]( https://github.com/JeroenSimonse/MachineLearningProject )

This project was part of our Machine Learning course and consisted of the following two tasks:
1. Image classification
	* Using and testing MLP and CNN models
2. Using the best performing classifier from task 1, to identify a series of five letters in one image

The models from task 1 were trained and tested on the MNIST dataset. For the second task, our professor a custom dataset. 

## Results
For the image classification the CNN model performed best, and scored an accuracy of ~95%. The MLP models scored slightly worse, and scored an accuracy of 92%.
For the second task a sliding window was applied to the images, however this didn't work properly, as the letters appeared in random places and could even overlap eachother. 

CNN Accuracy:

![CNN Accuracy](/images/cnnaccuracy.png) 


MLP Accuracy:

![MLP Accuracy](/images/mlpaccuracy.png) 

