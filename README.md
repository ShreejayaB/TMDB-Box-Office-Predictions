<center><h2>TMDB Box Office Revenue Predictions</h2></center>


----
Description
----

This repo was made as part of project work done for Machine Learning Laboratory(MSDS 699) course at University of San Francisco's Master's in Data Science program. 

The data we have chosen was taken from a Kaggle competition https://www.kaggle.com/c/tmdb-box-office-prediction/data

Contributors:

- Akanksha https://github.com/akanksha1304
- Aakanksha https://github.com/aakanksha-ns
- Shreejaya https://github.com/ShreejayaB

----
Goal
----
The goal of our project was to predict the revenue of movies at the box office.

----
Process
----

1. Data processing which included missing value imputataion and encoding categorical features.
2. Feature engineering - deriving meaningful features like age of the movie.
3. Building pipeline to fit various machine learning models.
4. Evaluating the models using relevant metrics and defining a North Star metric.
5. Choosing the best model and visually inspecting our results. 

----
Summary 
----
For our problem statement we chose a baseline model as a linear model (Ridge Regression)<br>
We fit the following models to our data:<br>
1. Ridge Regression
2. KNeighboursRegressor
3. BayesianRidge
4. RandomForestRegressor
5. XGBoost

Out of these models, we observed that RandomForest model performs the best - <br>
1. MedAE score(in million$) - 15.02<br>
2. R2 score - 0.73<br>
3. RMSLE - 2.66<br>

#### Takeaways:
1. Difficult to accurately predict the movie’s box office performance because of various missing data points such as:<br>
	Overall economy at the time of the movie release<br>
	Quality of the movie’s plot and other exogenous factors<br>
	Presence of streaming service like Amazon Prime, Netflix etc.<br>
2. Log transforming the response (Revenue) might help.


In order to run our notebook and reproduce the results, the following steps can be followed:

### 1) Setup
Clone the repository using the given link: https://github.com/aakanksha-ns/ml_lab_project_box_office_revenue.git
### 2) Creating Virtual Environment
* Run the following command to create the virtual environment named 'tmdb_box_office_pred_ml':
conda env create -f tmdb_box_office_pred_venv.yml -n tmdb_box_office_pred_ml
* Activate this virtual environment with the following command:
conda activate tmdb_box_office_pred_ml

### 3) Start IPython
Start the IPython notebook server from the root directory, with the 'jupyter notebook' command.