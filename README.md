(https://lever-client-logos.s3.amazonaws.com/d3dff7b3-cda9-4dea-8369-e4a757ec81a1-1505217546657.png)

# Springboard Data Science Mini-Projects

Welcome! This repository contains my data science mini-projects, ranging from data wrangling and statistical inference to machine learning and advanced data visualization.

### Data Wrangling

**[JSON Exercises](https://github.com/ameen-abdelghani/Springboard/blob/master/Json_Assignment/JSON_Assignment_Ameen_Abdelghani.ipynb):** The dataset on the World Bank projects is available in a JSON file. I first load the data as a Pandas dataframe and find that China, Indonesia and Vietnam have the most projects with the World Bank. Then I load the JSON file as a string, normalize the project themes, and find that environment and natural resources management, rural development and human development are the project themes with the highest frequencies. 


### Exploratory Data Analysis

**[Human Body Temperature](https://github.com/ameen-abdelghani/Springboard/blob/master/Exploratory_Data_Analysis/EDA_human_temperature/sliderule_dsi_inferential_statistics_exercise_1.ipynb):** 
Using a dataset of human body temperatures to illustrate the concept of Central Limit Theorem, hypothesis testing with one sample or two samples, and confidence intervals.

**[Racial Discrimination in US Job Market](https://github.com/ameen-abdelghani/Springboard/blob/master/Exploratory_Data_Analysis/EDA_racial_discrimination/Racial_Discrimination_Prjoect.ipynb):** The dataset comes from a field experiment in which researchers randomly assign identical resumes with black-sounding or white-sounding names and observe the impact on requests for interviews from employers. Resumes with black-sounding names receive a callback rate of 6.4%, while white names receive a callback rate of 9.7%. This difference of 3.3 percentage points is statistically significant, as the p-value for the test of equality of callback rates is less than 0.001. Moreover, the 99% confience interval suggests that the true callback rate difference could range from 1.2 percentage points to 5.2 percentage points. Therefore, racial discrmination in the U.S. labor market still appears to be a continual challenge.

**[Recommendations for Reducing Hospital Readmissions](https://github.com/ameen-abdelghani/Springboard/blob/master/Exploratory_Data_Analysis/hospital_readmit/sliderule_dsi_inferential_statistics_exercise_3.ipynb):** Hospital readmissions have been used as indciators of poor quality of care, such as inadequate discharge planning and care coordination. The goal of the Hospital Readmissions Reduction Program is to reduce such unnecessary and avoidable readmissions.
The initial report suggests taht hospitals with smaller number of discharges tend to have a higher excess readmission ratio. But it does not report the correlation coefficient or test whether the correlation is statistically significant. I improve the analysis by finding that the Pearson correlation coefficient is -0.09, suggesting a negative but small correlation between the number of discharges and excess readmission ratio. The p-value of the correlation test is less than 1%, so this negative relationship is indeed statistically significant. However, since the correlation is so small, it is not practical to assume that hospitals with smaller number of dischrages will always have a higher excess readmission ratio. As a result, I do not recommend that hospitals with smaller capacity be required to upgrade their resources or facilities.

### Machine Learning

**[Linear Regression with Boston Housing Dataset](https://github.com/ameen-abdelghani/Springboard/blob/master/Machine_Learning/Mini_Project_Linear_Regression.ipynb):** I use `scikit-learn` library to build a linear regression model to predict the housing prices in Boston. The various features include per capita crime rate, average number of rooms per dwelling, and pupil-teacher ratio by town. I also split the data into training and testing sets in order to measure how well the model built with the training set can predict the 'unseen' data in the test set. I show how multiple rounds of cross-validation performed on different partitions help limit the problem of overfitting a particular training subset and thus reduce variability of the model.

**[Classification and Logistic Regression](https://github.com/ameen-abdelghani/Springboard/blob/master/Machine_Learning/Mini_Project_Logistic_Regression.ipynb):** I use cross-validation and grid search to find the best regularization parameter **C** for the logistic regression. Regularization applies a penalty for increasing the coefficient estimates in order to reduce overfitting. The regularization parameter **C** in `scikit-learn` is the inverse of the shrinkage parameter lambda. Larger lambda or smaller **C** increases the shrinkage pentalty and shrinks the coefficient estimates toward zero. By default scikit-learn sets **C=1** in logistic regression, so some amount of regularization is used even if **C** is not specified. Regularization is good at reducing the variance of the predictions but increasing the bias at the same time. `GridSearchCV` performs a cross-validated grid-search over a parameter grid. We need to specify an estimation method, parameter values for the estimator and a scoring method. The results show the best estimator, the score of the best estimator, and the parameter setting that yields the best score.

**[Text Classification with Naive Bayes](https://github.com/ameen-abdelghani/Springboard/blob/master/Machine_Learning/naive_bayes/Mini_Project_Naive_Bayes.ipynb):** I analyze the movie reviews from the rotten tomatoes database. The goal is to train a classifier to predict whether a critic's movie review is 'fresh' or 'rotten.' To preprocess the text, `CountVectorizer` allows us convert the collection of movie reviews into a matrix of token counts. The parameter `min_df` is used to removed terms that are too rare, and `max_df` is used to remove terms that are too common. I then train a multinomial Naive Bayes classifier assuming that features are conditionally independent given the class. In Naive Bayes, alpha is an additive (Laplace/Lidstone) smoothing parameter. A larger alpha will reduce the variance of the model (and overfitting) but increase bias at the same time. We can think of alpha as a pseudocount of the number of times a word has been seen. In the following code, I use grid search to find the best alpha as well as the best `min_df` that will maximize the probability of observing the training data.

For feature selection, we can create an identity matrix with the size of the number of features/words, each row representing exactly one feature/word. We then use any one word to predict the probabilitiy of freshness or rottenness of a review that contains this word. If one single word can generate high probability of a review being fresh or rotten, that implies this feature has a high predictive power. Reviews containing words such as perfect, touching and masterpiece are likely to be fresh, while words like unfortunately, dull and worst tend to predict rotten reviews.


**[Customer Segmentation using Clustering](https://github.com/ameen-abdelghani/Springboard/blob/master/Machine_Learning/clustering/Mini_Project_Clustering.ipynb):** The dataset contains wine offers that were e-mailed to the customers and data on which offers they purchased. Important features of wine offers include wine varietal, the minimum quantity, discount, country of origin and whether or not it is past peak. I merge two spreadsheets and create a pandas dataframe with each row representing a customer and each column representing a wine offer. I first apply K-Means Clustering and use both the elbow method and the Silhouette method to choose the number of clusters. To visualize the clusters, I use Principal Component Analysis to reduce the 32 features into two dimensions. I also compare results from other clustering algorithms: affinity propagation, spectral clustering, agglomerative clustering, and DBSCAN. 

From here I observe the differences in each clusters tastes, by observing the ads they clicked on and which wine variant the ad showed. I validated that each cluster had very different tastes for wines, and with this information the marketing department can design more cost effective and influential ad campaigns to target specific customer segments.
