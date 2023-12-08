# Practical-Application-2   

### Link to the notebook   
[Link to the notebook](https://github.com/lis-assignment/Practical-Application/blob/main/prompt_II_3%20copy.ipynb)   

---   
##### What drives the price of a car?
![](images/kurt.jpeg)   

### Modeling Conclusion   
The current used car dataset is high-dimensional and contains polynomial features.
Before applying multiple regression models, it is required to transform non-numeric features using get_dummies function and scale the data for the best results.   
For processing training and testing sets, as the squared error will increase the price difference, it is necessary to use numpy.log function to rescale price (y sets)   
Sequential feature selection (greedy algorithm) and GridSearchCV are used to process the hyperparameter and produced the Train MSE (0.3768) and Test MSE (0.3768)   
Ridge regularization is faster than Lasso regularization and more numerically stable. For this dataset, Ridge showed Train MSE (0.352) and Test MSE (0.353)   
Lasso regularization automatically performs feature selection   
After the comparison, the best model is Sequential feature selection and the best 5 features are: year, odometer, honda, nissan, ram   

### Evaluation

With some modeling accomplished, we aim to reflect on what we identify as a high quality model and what we are able to learn from this.  We should review our business objective and explore how well we can provide meaningful insight on drivers of used car prices.  Your goal now is to distill your findings and determine whether the earlier phases need revisitation and adjustment or if you have information of value to bring back to your client.   

### To increase the data quality and model prediction   
* Data cleaning and preparation is implemented to remove outliers, fill null values, keep important features   
* Top 10 manufacturers are kept to analyze the main market
* Several types of plotting provides valuable information: market percentage, year and odometer histogram   
* Model selection requires non-numeric features, standarization, and pice log transformation  
* Three models (Sequential feature selection, Ridge regularization, Lasso regularization) were processed,and GridSearchCV is used to optimize the hyperparameter   
* The best model is sequential feature selection and the best 5 features are: year, odometer, honda, nissan, ram   
### Deployment

Now that we've settled on our models and findings, it is time to deliver the information to the client.  You should organize your work as a basic report that details your primary findings.  Keep in mind that your audience is a group of used car dealers interested in fine tuning their inventory.   

### In this report, the real-world used car dataset is analyzed using multiple regression models to provide valuable information for the car dealers. 
To investigate the best factors to affect the car price, important steps are implemented: 
* Data observation indicates that there are mixed data types of columns and unrealistic outlier numbers for price, year and odometers. Moreover, high ratio of null values will affect the data quality. 
* Therefore, in order to understand the used car market, the dataset is cleaned and transformed with the 
data cleaning and preparation methods, and the null values are replaced with 'unknown'.   
* Since the top 10 manufacturers takes about 70% of the business data, it is important to focus the analysis into this field.      
* Different types of plotting provide general and statistic pictures for the main market, which can also help to increase the total data quality. 
   
The real-world data demonstrates high-dimensional and polynomial features. After comparing several multiple regression models, the powerful machine learning choosed the sequential feature selection as the best model, and recommended 5 best features: year, odometer, honda, nissan, ram. 
The final results demonstrated that: among all the factors, the most important feature is the year to affect the car price, the newer the better, secondly the lower odometer, the higher the price. Then in the top 10 brands, the honda and nissan keep the highest car values.

