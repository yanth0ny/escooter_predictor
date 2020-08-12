## Main Task

The main goal is to predict the total number of active e-scooter users given the available
attributes.


## Data Description

- `date` Date in YYYY-MM-DD.
- `hr` Hour (0 to 23).
- `weather` Description of the weather conditions for that hour.
- `temperature` Average temperature for that hour (Fahrenheit).
- `feels_like_temperature` Average feeling temperature for that hour (Fahrenheit).
- `relative_humidity` Average relative humidity for that hour. Measure of the amount of water in the air (%).
- `windspeed` Average speed of wind for that hour (arbitrary units).
- `psi` Pollutant standard index. Measure of pollutants present in the air (0 to 400).
- `guest_scooter` Number of guest users using the rental e-scooters in that hour.
- `registered_scooter` Number of registered users using the rental e-scooters in that hour.
- `guest_bike` Number of guest users using the rental e-bikes in that hour.
- `registered_bike` Number of registered users using the rental e-bikes in that hour


 
## Strategy Summary

This dataset is a data from an unknown country from the period 2011 to 2012. In this dataset, some of the features presented are weather information such as weather conditions, humidity level, psi level, and temperature. This dataset focus on registered and guest users of the eScooters rental, which put together is our target variable, total active users. The objective of this exercise is to use the existing data to forecast demand for eScooter rental in the coming years. 

The process of this exercise starts from data preprocessing, analysis and EDA, features engineering, modeling, validation, and finally to deployment. During data preprocessing, we uncover human errors and abnormalities such as null value, repeated values, missing values, and incorrect entries. The purpose of doing this is to increase data integrity so we can have a more accurate model to work with. During data analysis, we look for insights to help us select the 'right model' (most effective) based on the insights we analyzed.  In this dataset, we can see one of the key aspects is the time series, which we can use to help us forecast future demand. Another interesting aspect that we can see is that only temperature, humidity, and psi is well correlated with our target variables. And using the various plots, we are able to understand the different characteristics of this dataset.

In features engineering, we prepare the data to be trained by the selected model. This includes filling in missing values which we did manually and also removing outliers. This helps us to increase model accuracy.

The model chosen here is XGBoost. This is because of the time required to train this model while maintaining high accuracy. At the same time, this model allows us to use multivariable and allows us to forecast well into the future. For validation, we plot a scatter plot of the predicted against the actual results and collect the summary. From the summary shown in the notebook, we only need to focus on MAE, RMSE, and R square.  

Lastly, we convert the notebook into code that can ideally be reused to increase its economical value.


## Steps

Data extraction
- Accessing the server
- Selecting specify data to collect
Exploratory Data Analysis (EDA)
- Data overview
- Handling abnormalities
- Preprocessing
Visualization
- Pair plots
- Cluster map
- Line plots
- Bar plots
- Scatter plots
- Box plots
Insights
Machine Learning
Featured Engineering
- Box plots
Model Selection
Validation Metrics
Univriante Time Series Analysis
- Out of Sample Forecast
XGboost
- Out of Sample Forecast



## Files:

eda.ipynb			: Exploratory Data Analysis (EDA) of this dataset
main.py				: The first file executed by run.sh. User will be ask to select a few options.
model_training.py	: main.py will execute this program for model training process. 
requirements.txt	: packages required
Readme.md			: This file.




## Authors & License

* **Anthony Lin**
