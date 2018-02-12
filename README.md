# Analytics_Vidhya_01132016

In this project, I use a data set from analytics vidhya competition from January 12, 2018. The more information about the competition can be found [here](https://datahack.analyticsvidhya.com/contest/analytics-vidhya-hiring-hackathon/) .
You will need to create an account and login to read the full problem statement.  


## About the Data 
The problem statement describes the data as hourly electricity information for an electricity company. The company is looking to find a trend between electricity consumption and weather information. The data contains the electricity consumptio (target), unique ID, date time of record, temperature , pressure, windspeed, and two anonymized features. 
The goal is to predict the electricity consumption by using the other variables. 

The training data is the first 23 days per hour of each month while the test set is the 24th to the end of the month. 
The public leaderboard on the site is the first 2 days while the private leaderboard is the remaining set. 
Unfortunately I was unable to submit scores for this competition. We can still compare the model performance using other measures. 

## EDA 
Exploratory Analysis was conducted on the data set to understand more about the data. This analysis is in the notebook [here] (https://github.com/malctaylor15/Analytics_Vidhya_01132017/blob/master/Analytics%20Vidhya%2001-12-17.ipynb). By plotting the variables, we acan see the cyclical and non cyclical patterns in the variables. There are clear patterns and spiking behaviours in the different variables. We also find that one of the anonymous variables is categorical.  

Plots of different time aggregations are also used to help understand the the variables. Min-max ratio, standard deviation, average of each month are also examined. 

More daily analysis could have been co in consumption could have also been conducted to understand when the spikes occured.   

## Data Preparation

To prepare the data, we one hot encoded var2 into the 3 separate encodings. There is not a definition for the variable, we will just have to use the encodings as are. 
We also one hot encode the date time into 12 variables for each month. 

Due to the large amounts of data, we more variables could have been generated. More variables about time and interaction variables could have been made. 

## Linear Regression 

We look at the linear regression results and look at the coefficients. Due to the different scale of the variables it can be difficult to directly compare the coefficients. We might be able to do more analysis on the month coefficients.

The validation set is 25% of the training set. We use R2 and RMSE as out evaluation metrics. We find that the different between the test and train sets is less than 1%. 




