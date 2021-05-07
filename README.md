# Manhattan-Taxi-Forecasting

Welcome to one of my many senior projects (and probably favorite!) where I use data analysis and machine learning to solve a real-world problem. 

Now that we have Uber & Lyft, we can finally tell just how long it'll take to get to our final destination when ride-sharing. How do they know?! Well, good  predictive models! In this project I explore NYC taxi data for how features can be used, or new ones engineered, to train and test different types of models that predict taxi ride duration. In the end I check each model's performance and choose the most successful. Below is a more detailed breakdown of my work throughout each stage of the data science lifecycle. Hope you enjoy!

1. Data Selection and Cleaning

  - queried a SQLite database for NYC taxi data
  - narrowed the scope to rides where pick up and drop off were inside a polygon that defines the boundaries of Manhattan
  - cleaned the data by eliminating negative passenger counts, filtering for positive distances & rides that lasted between 1min and 1hr 
  
2. Exploratory Data Analysis

  - identified atypical days in January and found two events that led me to remove data from these days: historic blizzard that shut the city down for a couple days & Jan 1st landing on a Friday (a usually busy weekday)
  
3. Feature Engineering

  - created new features to enhance information provided to model:
   
     - explored target feature: ride duration by day/hour/period of day 
     - used PCA to rotate geolocation data and label data points by region of lower Manhattan, midtown, and upper Manhattan 

4. Model Selection

  - compared RMSE of a constant model, simple linear regression model considering only distance, an unregularized linear regression model considering all, and 2 decision tree regression models split by period and region
  - best model was a decision tree regression model split by period of day (morning, afternoon, evening)
 
