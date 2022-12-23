# Bike-Sharing-Demand-Prediction

## Table of Content

1. Introduction

2. Problem Statement

3. Dataset Information Tools and Technologies used

4. Steps involved

5. Algorithms used

6. Conclusion

## 1. Introduction

Bike sharing is an innovative way to provide individuals with bicycles for their temporary use for a fee or for free. Globally, bike-sharing systems have gained significant popularity in recent decades. The reasons for this are that it is environmentally friendly, convenient, and economical. Additionally, this system promotes healthier habits among its users and reduces fuel consumption.

#### The goals of this project are- 

Identify the key factors influencing rental bike demand hourly and examine the trends in the data.

Predict the number of rental bikes per hour using a regression model.

## 2. Problem Statement

Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.

#### Dataset information

The dataset contains weather information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation, Snowfall, Rainfall), the number of bikes rented per hour and date information.


#### Attribute Information:

* Date : year-month-day
* Rented Bike count - Count of bikes rented at each hour
* Hour - Hour of he day
* Temperature-Temperature in Celsius
* Humidity - %
* Windspeed - m/s
* Visibility - 10m
* Dew point temperature - Celsius
* Solar radiation - MJ/m2
* Rainfall - mm
* Snowfall - cm
* Seasons - Winter, Spring, Summer, Autumn
* Holiday - Holiday/No holiday
* Functional Day - NoFunc(Non Functional Hours), Fun(Functional hours)

## 3. Dataset Information Tools and Technologies used

The programming language used in this project is Python . The following libraries were used for data analysis and data visualization and to build a classifier to predict the price range of mobile phones.

Pandas : For loading the dataset and performing data wrangling

Matplotlib: For data visualization.

Seaborn: For data visualization.

NumPy: For some math operations in predictions.

Sklearn: For the purpose of analysis,prediction and evaluation.

## 4. Steps involved

Exploratory Data Analysis : Performed Univariate, Bivariate, and Multivariate analysis with various graphs and plots to better understand the distribution of features and their relationships.

Feature Extraction : Created new columns such as Day, Month, Year, day_of_week and day_of_month from Date column .

Feature Selection : Checked the VIF value (measure of multicollinearity) and dropped Dew point Temperature and Year which were highly correlated with other independent features.

Feature encoding : The categorical features present in the dataset Seasons, Holiday, Hour were ordinally encoded.

Feature Scaling : Brought features to a similar range using Standarisation.

Implementation of Regression models

Comparision of models

## 5. Algorithms used

Linear Regression

Regularisation - Lasso, Ridge

Decision Tree Regression

Random Forest Regression

## 6. Conclusion

#### Data Exploration Conclusion:

* Temperature: People generally prefer to bike at moderate to high temperatures. We see highest rental counts between 20 to 32 degree Celsius.
* Humidity: With increasing humidity, we see decrease in the number of bike rental count.
* Hour: Bike rental count is mostly correlated with the time of the day. As indicated above, the count reaches a high point during peak hours on a no holiday and is mostly uniform during the day on a non-holiday.
* Temperature, Windspeed, Visibility, Solar radiation: They have a positive correlation with bike rents.
* Rainfall, Snowfall: They have a negative correlation with bike rents.
* Seasons: We see highest number bike rentals in Summer and the lowest in Winter season.

#### Modeling Conclusions:

* We use 5 Regression Models to predict the hourly rented bike count - Linear Regression, Lasso, Ridge, Decision Tree, Random Forest.
* Among all the 5 models, Random Forest Model has the best metric analysis.
* Lasso or Ridge regularisation did not provide any improvement to the regular linear regression.
