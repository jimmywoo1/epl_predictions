# EPL Predictions
Predictions on English Premier League standings using a linear regression model based on historical dataset from seasons 2005-2006 to 2018-2019 (raw data can be found [here](http://www.football-data.co.uk/data.php)).

# Prerequisites
The following are the python libraries used for this project:

glob2==0.6  
keras==2.2.3  
matplotlib==2.2.2  
numpy==1.14.3  
pandas==0.23.0  
scikit-learn==0.19.1  
seaborn==0.8.1  

# Overview
* [raw_data](raw_data) - contains all raw csv files for EPL and EFL seasons
* [data](data) - contains all preprocessed csv files for EPL seasons
* [src](src) - contains code for processing and analyzing results

# Approach
In this project, I implemented a linear regression model using the season aggregate statistics of a team performance from seasons 2005 - 2006 to 2018 - 2019, to predict the performances of the 20 EPL teams in the 2019 - 2020 season. The exploratory data analysis (EDA) on the dataset, data preprocessing, and the results of the regression model can be found in [preprocessing.ipynb](src/preprocessing.ipynd) and [models.ipynb](src/models.ipynb)

# Results
The implemented model is only able to provide realistic predictions for teams that have consistent performance from the previous year to the 19/20 season. For teams that are performing significantly different from the previous seasons, the model fails to provide useful predictions. This is likely due to the fact that the premier league is such a complex beast to model, aggregated statistics from the previous season alone is not going to provide enough information, and thus our model cannot capture the complexity of the problem. A larger set of more relevant features may help improve the performance of the model (e.g. amount spent in transfer market, quantified metric of manager competency, existence of star player in squad), but it is likely that a lot of useful information is lost by using aggregate statistics of the entire season. For future work, making predictions at the game-level instead of the season-level will likely yield better results. 
