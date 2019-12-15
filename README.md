# Google-Search-Trends-and-S-P-500
In this repository, I have fetched google search trends data of search terms that are related to the stock market and have made a linear regression model in order to see which search terms are highly significant.

How to run the files?

The files can be uploaded to jupyter notebook cloud (No installations) or opened using anaconda navigator. 
Upon uploading the files, recheck the file paths under the "Paths" markdown in the jupyter notebook. (Especially for the 2008 model)

Findings : 

It turns out that price has the highest correlation with debt, bull market and economic boom. And of course, it has a high correlation with DummyTime because the price is going up (mostly) with time. 

In order to find which search term is highly significant and which one is not, I decided to run a multivariable regression. 

Single Variable Regression : y = mx+b
Multi Variable Regression: y = mx1 + mx2 + mx3 … + b

Here, the ‘x’ represent the search terms and y represents the price (explanatory and response respectively)

For the 2004 - Present model : 

The train data R squared value is high while the test data R squared is low. 
This is because our model was trained with the train data and made so that it fits well with it. 
While for the test data, a data that our model didn’t see before, the model does not fit too well. 
This is logical because the real world data will always have variance and may not fit the regression properly. 
According to the first info, 92% of the price action is explained by the search terms and dummy time for training data. 
For the test data, 52% of the price action is explained by the search terms and dummy time.

For the 2008 weekly model : 

Training data R squared 0.8816992296795523
Testing data R Squared 0.6010514258458983

Improvements that could be made:

Firstly, we found out that the R squared for the test dataset if too low, we could improve this by using larger datasets with more search terms. 

Check for multicollinearity : Some search terms could be highly correlated with each other and might have less correlation with the price itself. If such search terms are removed after considering their p values, I believe the model will fit the test data well. 
Search trends from other search engines could be used to get a bigger picture and to make important distinctions.

 Web traffic in trading sites, news source could also be used for a better prediction of the price. 

