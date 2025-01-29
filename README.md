# Bike Sharing Prediction MLR Model
> A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state.
> The company wants to know:
Which variables are significant in predicting the demand for shared bikes.
How well those variables describe the bike demands


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- Using a multiple linear regression model, we aim to help BoomBikes identify the key predictors that could increase their revenue and enhance their business among customers.
- BoomBikes, a USA-based company, experienced a dip in revenue during the COVID-19 pandemic and wants to understand the various factors contributing to this decline. By applying a multiple linear regression model to the dataset, we will predict the bike rental count using several key features.
- For this analysis, we are using the bike sharing dataset provided by the company, specifically the file day.csv.
<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
- Univariate Analysis :
  1. Categorical columns
    - In the fall season, the highest number of bike rentals is 188, compared to other seasons.
    - We can observe that for both years 2018 and 2019, the number of bike rentals are same.
    - As per the data, alternate months starting from January show an increase in the number of bike rentals. However, in July and August, the number of bike rentals remains the same. The lowest bike rentals   
    occurred in February.
    - 709 bike rentals were done on a working day as compared to holidays.
    - Almost all weekdays have same number of bike rentals.
    - A total of 499 bike rentals occurred on working days rather than holidays or weekends.
    - The highest number of bike rentals occurred during clear weather conditions.
  2. Numerical columns
    - The highest number of bike rentals occurred when the temperature was between 25 and 30 degrees Celsius.
    - The highest number of bike rentals also occurred when the feels-like temperature (apparent temperature) was between 25 and 30 degrees Celsius.
    - According to the data, bike rentals peaked when the humidity level was around 60%.
    - The highest number of bike rentals occurred when the wind speed was between 10 and 15 km/h.
    - The majority of total bike rental counts fell between 4000 and 6000.
- Bivariate Analysis :
  1. Categorical columns VS Cnt
    - In the season of fall, the number of bike rentals were the highest as comapred to other season's.
    - In the year 2019, bike rentals reached their peak.
    - The months of June and September saw the highest number of bike rentals.
    - As per the data, highest number of bike rentals were done during working days.
    - There is an increasing trend in bike rentals from Sunday to Friday.
    - Bikes were rented more frequently on working days than on holidays or weekends.
    - Clear weather conditions were the most favorable for bike rentals.
  2. Numerical columns VS Cnt
    - We can observe positive correlation between temperature and cnt as well as feels-like temperature and cnt.As the temperature and apparent temperature increases, there is also an increase in the count 
      of bike rentals.
    - For humidity, we can see wide distribution of bike rentals count.
    - Windspeed between 5 to 25 km/hr also shows distribution with count ranging upto 8000.
- Final Model building Observation
    Using RFE approach, we selected the top 15 independent variables. Then we proceeded with manual approach and build the model with 15 variables.
    Using statsmodel, we build the model where we got the adjusted R square as 84.3 %
    We noticed that variable Fall had high pf and vif value, so we dropped it and build the model again.
    In the final model, the adjusted R square remained the same indicating variable Fall was a insignificant variable.
    After building the final model, all the pvalues for independent variables were below 0.05 and vif was below 5.
    The F-statistic for the final model had a very small p-value (8.70e-192), indicating a highly significant fit among the variables.
- Analysis on Test Data
    The R square score on the test data is 81.4%, and the R square score on the training data is 84.8%.
    The difference between the R square scores of the training and test data is 3.4%, indicating that the model has performed well on the test data.
- Summary
    Temperature has the strongest correlation with bike rental count (cnt) stating that when the temperature increases the bike rental count will also increase.
    In the year 2019, bike rentals significantly increased compared to 2018, showing substantial boom in Boombikes' business.
    Bikes were rented the most during the winter and summer seasons.
    Months August,September,October contrbuted the most to bike rental count.
    Among the months analyzed, September had the highest positive impact on bike rental counts, while August and October had smaller, yet positive contributions.
    Cloudy weather and light snow have a negative impact on bike rental counts. Additionally, humidity and windspeed also negatively affect bike rentals.
    Both Saturday and working days have a positive effect on bike rental counts.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- library - version 1.0
- library - version 2.0
- library - version 3.0

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- This project was inspired by...
- References if any...
- This project was based on [this tutorial](https://www.example.com).


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
