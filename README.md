
**BUILDING A MOVIE RECOMMENDATION SYSTEM USING COLLABORATIVE FILTERING**
​
This repository contains the following
​
* A Jupyter notebook
* A non-technical presentation.
* A CRISP-DM report
* A README file
* MOVIELENS data
​
**BUSINESS OVERVIEW**
​
Developing a recommendation system based on user ratings that can enhance user satisfaction, engagement, and revenue generation for the XMOVIES platform. The system should leverage data science techniques to analyze user preferences and generate accurate and personalized recommendations, thereby increasing user retention, driving user interaction, and boosting overall platform usage.
**DATA**
The project uses the MovieLens dataset from [MovieLens](http://movielens.org) , which contains the following files;
​
* links data
* tags data
* movies data
* ratings data
​
The MovieLens dataset provides a rich and reliable source of movie ratings and associated information, making it a suitable choice for building and evaluating movie recommendation systems.
​
COLLABORATIVE FILTERING
​
collaborative filtering was used in the Reccomdation system and it involved the following steps
1. Converting the DataFrame into a Surprise Dataset
2. Splitting the data into training and testing sets
3. Hypertunning Dataset to get the best parameters by Performing a gridsearch with SVD
4. Cross-validating with KNNBasic
5. Cross-validating with KNNBaseline
6. Model evaluation using RSME and MAE
7. Making predictions
8. Testing the reccomendation systems
​
**COLLABORATIVE FILTERING RESULTS**
* The KNNBaseline algorithm indicated a lower RMSE of 0.8774070745386995, which suggests better prediction accuracy compared to KNNBasic.
* The KNNBasic algorithm indicated a higher RMSE of 0.9730103781790413, indicating a slightly higher prediction error.
​
Based on the RMSE values provided, KNNBaselineoutperformed KNNBasic in terms of prediction accuracy and recommendation quality.
​
**IMPROVING THE RECOMMENDATION SYSTEM**
​
The following techniques were adopted to try and improve the RMSE and MAE of the model;
**1. Ensemble methods**
​
The previous collaborative filtering model built using SVD, we got 'rmse': 0.8693804004379402, 'mae': 0.6684190070988877 looking at the result of the ensemble method, RMSE: 0.8860305908074744 and MAE: 0.6800762378176585 meaning an RMSE increase of 0.01665019 
​
**2. Matrix factorization**
​
The previous model built, we got 'rmse': 0.8693804004379402, 'mae': 0.6684190070988877 looking at the result of the matrix factorization using ALS method we get Average RMSE: 0.9778 and Average MAE: 0.7535 meaning an RMSE increase of 0.1084196
​
**3. Collaborative filtering using baseline only**
​
The previous collaborative filtering model built using SVD, we got 'rmse': 0.8693804004379402, 'mae': 0.6684190070988877. The Baseline model gives RMSE: 0.8744 which an increase of RMSE with 0.0050196 which is not a significant difference
​
**4. Hybrid system using both collaborative and content filtering**
​
The previous collaborative filtering model built using SVD, we got 'rmse': 0.8693804004379402, 'mae': 0.6684190070988877. The Hybrid strategy gives RMSE: 0.9433 which an increase of RMSE with 0.0739196
​
# CONCLUSION 
​
SVD and BaselineOnly had the lowest RMSE values indicating better prediction accuracy compared to the other models. 
​
# RECCOMMENDATIONS
​
* As SVD and BaselineOnly model had the lowest RMSE and relatively low MAE values, meaning they are both a good option for the collaborative filtering recommendation system, we recommend comparing these two models based on other metrics, such as coverage and diversity, to make a final decision.
* The ensemble model also performs well with a slightly higher RMSE compared to SVD. As this model allows for diversity and variety in recommendations, we recommend applying the ensemble model and seeing how it performs on the recommendation system.
* The Hybrid strategy that combines collaborative filtering and content-based filtering is a good alternative option although it has a higher RMSE compared to SVD, we recommend further investigation and fine-tunning this strategy to improve its performance.
