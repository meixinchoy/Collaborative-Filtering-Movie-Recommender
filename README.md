# Collaborative-Filtering-Movie-Recommender

## About  
This Collaborative Filtering Movie Recommender explores recommenders that uses matrix factorization techniques to generate recommendations. Here, SVD is used to predict the rating of a particular user for a particular movie. Two programs were created for this, both written in the Python programming language. The first set of code ```svd-movie-prediction-and-recommendation.ipynb``` is created to predict the ratings and generate recommendations for a particular user using SVD while the second set of code ```svd-movie-prediction-evaluation.ipynb``` is created to evaluate the accuracy of the prediction made by the first program using cross validation. Parameter tuning is also demonstrated in ```svd-movie-prediction-evaluation.ipynb```.

Dataset: [MovieLens 20M Dataset](https://www.kaggle.com/grouplens/movielens-20m-dataset)

## Matrix Factorization
Matrix factorization solves two of the biggest issues in memory-based CF (scalability and sparsity) by decomposing the original sparse matrix into lower dimension matrices that are less sparse. The benefit of using matrix decomposition is that even if two users have not rated the same items, the system can still find out the similarity between their taste and preference. 

The underlying reason behind the similar taste is also known as latent features or latent factors. For example, two individuals might recommended a particular book because of their preference in a specific genre. Hence, the latent feature for this recommendation is the genre of the book, such as romance, mystery and science fiction. Eventually, what matrix factorization cultivates is how much a user is aligned with a set of latent factors. Using matrix factorization, we can discover the latent factors that influence a person’s preference and predict the rating of a certain person to a particular product. 

### Singular Vector Decomposition
In this prototype, the matrix factorization used is Singular Vector Decomposition (SVD). SVD is a popular method in linear algebra for matrix factorization and dimensionality reduction. SVD transforms a higher dimension matrix into multiple lower dimension matrices that are a linear combination of the row or columns values, where the values in the original data matrix can be closely approximated.      
![image](https://user-images.githubusercontent.com/65379600/131359168-65ae5f58-86ff-46a3-85ff-32ea687ad611.png)

## Cross Validation 
Cross-validation is a resampling procedure used to evaluate machine learning models on a limited data sample. The procedure has a single parameter called k that refers to the number of groups that a given data sample is to be split into. As such, the procedure is often called k-fold cross-validation. learn more about cross validaion [here](https://machinelearningmastery.com/k-fold-cross-validation/#:~:text=Cross%2Dvalidation%20is%20a%20resampling,k%2Dfold%20cross%2Dvalidation.)

Using 10-fold cross validation, the given data sample is split into 10 subsamples to evaluate the model. Out of the ten subsamples, nine of the subsamples are used as training data whereas the remaining subsample is used as the test data to test the model. The cross-validation process is repeated for ten times with each of the 10 subsamples being used as test data exactly once.      
![image](https://user-images.githubusercontent.com/65379600/131431054-3956bb8a-1d01-4c26-9bbc-23d05b9cd85a.png)


## FIles
* ```svd-movie-prediction-and-recommendation.ipynb```   
  * Predict ratings for specific users using SVD   
  * Recommend movies with a high prediction rating    
* ```svd-movie-prediction-evaluation.ipynb```      
  * Evaluate accuracy of SVD model using RMSE and cross validation    
  * Parameter tuning to obtain optimal parameters to maximize RMSE    

## Packages used
* [Scikit Learn](https://scikit-learn.org/stable/)
* [Surprise](https://surprise.readthedocs.io/en/stable/)
