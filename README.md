# Salary-Prediction-Indeed

I used Python to solve this problem. This is because Python is a clean, easy to handle language that requires only a few lines of code.
The libraries I used include:
Pandas (to easily organize, explore, represent and manipulate data),
Matplotlib (to code 2 dimensional plots and graphs), 
NumPy (to manage arrays),
Seaborn (to draw informative and attractive statistical graphs),
Sklearn(contains efficient tools for machine learning modeling) 
 

To prepare the data I checked if there were any null values existing or any duplicate rows.
 I also checked for outliers by plotting box-plots.
Wherever outliers were found I dropped those rows through the inter-quartile calculation method.
The numerical columns were normalized using minimum and maximum processor objects.

I applied Ridge regression Machine Learning Method.
 
As the data-set provided was labeled, which meant I had to pick a supervised algorithm. Regression algorithms predict the output values based on input features from the data fed in the system, which suited my problem statement the most. Hence, I had to choose from various regression models.
I chose the Ridge Regression Method as it resulted in the least RMSE compared to the other models and because of multicollinearity between 2 or more of the predicted variables.
It also prevents over fitting as well as provides a trade of variance for bias.
c.The other models I considered were: Simple Linear, Lasso, Logistic and Random Forest Regressor. 
 

Ridge Regression Algorithm works by applying a penalizing term (reducing the weights and biases) to overcome over-fitting. It works by attempting at increasing the bias to improve variance. Therefore the model becomes less sensitive to changes in independent variables.
 
Yes, transformations and encoding were used. Normalization was done to the numerical columns while One-hot encoding was done to the categorical columns using the get_dummies method from pandas.
 
The yearsExperience and jobType features had the greatest impact on salary. While the major and industry features have the least impact on salary. I identified these by plotting a correlation matrix between all the features. The features with high positive values were proportionally related to the salary feature. While features with high negative values were inversely related to the salary feature. 
 

I trained my model by using the train_test_split() method to split the given data-set into 80% training set and the rest (20%) into the testing set. Then using the Ridge() method from sklearn.linear_model I trained the model with the independent features (X_train) as:  jobType,yearsExperience,major,industry,milesFromMetropolis and degree.
The issue that concerned me was if the data-set for training was enough for the model to learn.

The RMSE I estimate on my model is 19.
I created this estimate by using mean_squared_error() method from sklearn.metrics on the training data-set. 

          Other metrics other than RMSE include Mean Absolute Error (MAE.
          MAE is a more natural measure of average error, and (unlike RMSE) is unambiguous. Dimensioned evaluations and inter-comparisons of average               model-performance error, therefore, should be based on MAE.)
