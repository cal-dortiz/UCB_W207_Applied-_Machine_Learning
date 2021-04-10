Ames Iowa Housing Price Prediction
===========================
<img align="right" width="120" src="./images/berkeley.png"/>

#### Authors : [Dan Ortiz](https://github.com/cal-dortiz/) | [Dan Weitz](https://www.google.com) 


U.C. Berkeley, Masters in Information & Data Science program - [datascience@berkeley](https://datascience.berkeley.edu/) 

Spring 2021, W207 - Machine Learning - D. Schioberg, PhD <br>
Section # - Tuesday 4:00pm PDT

----

<img src="./images/Header.png" align="center">


Photo by [David McBee](https://www.pexels.com/@davidmcbee?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels) from [Pexels](https://www.pexels.com)

## Description

### About
This repo contains Ortiz and Weitz's housing price predictive model built off of the [Ames Housing Data](http://jse.amstat.org/v19n3/decock.pdf) compiled by compiled by Dean De Cock. Data was sourced from [Kaggle](https://www.kaggle.com/).

### Goal
Develope a model that predicts the housing price for each individual I.D. in the Test Data

### Key Performance Indicator
Model performance will be deteremend by Root Mean Square Error (RMSE) between the logarithm of the predicted value and the logarithm of the observed sales price.

### Final Ensemble Model Performance

[Ensemble Model](https://github.com/cal-dortiz/W207_Applied-_Machine_Learning/blob/main/Final_Project/Model%20Files/Ensemble.ipynb) performed with a root-mean-squared-error of 0.02139. This puts the model performance within the top 200 submissions out of 7894 total submissions.

[Image of Leaderboard]

### Contributing Model Performance 

|Model|Performance (RMSE)|
|-----|------------------|
|KNN|0.09322723804857086|
|Random Forrest|0.09322723804857086|
|AdaBoost Regressor|0.09322723804857086|
|Linear Regression|0.026558292311187268|
|Ridge Regression|0.02648945867526529|
|Elasticnet Regression|0.026504229524769187|
|Lasso Model|0.035909927409052335|
|Gradient Boost|0.03256724983099581|
|XG Boost|0.028530390677932824|


## Files

|Name|Description|
|----|-----------|
|[Train Data](https://github.com/cal-dortiz/W207_Applied-_Machine_Learning/blob/183fae86e5c0acd1937557404734a1df7b4172d4/Final_Project/Data/train.csv) |Data used to train the model|
|[Test Data](https://github.com/cal-dortiz/W207_Applied-_Machine_Learning/blob/183fae86e5c0acd1937557404734a1df7b4172d4/Final_Project/Data/test.csv)|Data used to test the model|
|[Data Doc](https://github.com/cal-dortiz/W207_Applied-_Machine_Learning/blob/183fae86e5c0acd1937557404734a1df7b4172d4/Final_Project/Data/data_description.txt)|Documentation regarding the data set|
|[Initial EDA](https://github.com/cal-dortiz/W207_Applied-_Machine_Learning/blob/main/Final_Project/Data%20Exploration%20Files/Exploratory%20Data%20Analysis.ipynb) | Initial Exploritory Data Analysis|
|[Attribute Impact Analysis](https://github.com/cal-dortiz/W207_Applied-_Machine_Learning/blob/main/Final_Project/Data%20Exploration%20Files/Parameter%20Correlation%20Assessment.csv)| Summary of findings of attributes correlation/association with SalePrice.|
|[Transformation Study](https://github.com/cal-dortiz/W207_Applied-_Machine_Learning/blob/main/Final_Project/Data%20Exploration%20Files/Transformations%20Study.ipynb)|Notebook to study transformations of nominal attributes|
|[Regression Models]() |Notebook that explores different regression models for development|
|[KNN Model](https://github.com/cal-dortiz/W207_Applied-_Machine_Learning/blob/main/Final_Project/Model%20Files/KNN%20Model.ipynb)|Notebook that explores KNN models for development|
|[Random Forrest](https://github.com/cal-dortiz/W207_Applied-_Machine_Learning/blob/main/Final_Project/Model%20Files/Random%20Forrest%20Dev.ipynb)|Notebook that explores Random Forrest and Boosted models for development|
|[Ensemble](https://github.com/cal-dortiz/W207_Applied-_Machine_Learning/blob/main/Final_Project/Model%20Files/Ensemble.ipynb)|Final Model - Compilation of development models|


## Data Cleaning Process
* What we took out
* What we altered (setting 0)
* How we processed numerical
* How we processed ordinal
* How we processed catagorical

## Model Construction
* Discuss ensemble models and why we choose it

The final model is an ensemble of nine indipendent models. <br>

<img src="./images/model_vis.png" align="center"> <br>

The estimated housing price is the mean of the output of all nine models.

## Required Technologies
* Python 3.7
* Pandas
* Numpy
* XGBoost
* SkLearn
* MatPlotLib

## Credits
* Data Source: Kaggle
* README template: [Cristopher Benge](https://cbenge509.github.io/) | [William Casey King, PhD](https://jackson.yale.edu/person/casey-king/) 
License
-------
Licensed under the MIT License. See [LICENSE](LICENSE.txt) file for more details.