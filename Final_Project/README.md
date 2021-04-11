Ames Iowa Housing Price Prediction
===========================
<img align="right" width="130" src="./Images/berkeley.png"/>

#### Authors : [Dan Ortiz](https://github.com/cal-dortiz/) | [Dan Weitz](https://github.com/djweitz) 


U.C. Berkeley, Masters in Information & Data Science program - [datascience@berkeley](https://datascience.berkeley.edu/) 

Spring 2021, W207 - Machine Learning - D. Schioberg, PhD <br>
Section # - Tuesday 4:00pm PDT

----

<img src="./Images/Header.png" align="center">


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


<img src="./Images/kaggle_leader_board.png" align="center">
Kaggle Leaderboard 4/10/21


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
Each of the nine models may have slight adjustments to the describe procedures, however the below process is fairly representitive of the data cleaning procedure.

The initial data set consisted of 80 attribures, including the sale price. Both 'ID' and 'MiscFeature' were immediatly removed from the data set due to a lack of meaningfull contribution to the data set. In addition, we removed 5 outlires ferom the data. These houses had in excess of 4000 sqft of GrLivArea (Per the pencil notes in the data documentation). This resulted in a 25% decrease in regression RMSE.

Once this data was removed, the data needed to be further processed to assess missing data and build new attributes from the existing data. The initial swee to correct missing data was done according to the [data documentation](). For some attributes, 'NaN' was a valid data point and indicated the property did not have that feature. These empty data points were processed when converting the ordinal data into a machine readable state. Missing nominal data, was set to 0. This decision was made in the interest of time and is an identified opportunity for future improvements.

Numerical data was rescaled in some models and not processed in others. All ordinal data was encoded in a 0-5 scale, preserving the scaling relationship the data points had and catagorical data was encoded with dummy variables.


<img width="400" src="./Images/saleprice_logsp.png"/>

[ADD GRAPHS OF Y AND LOG Y. DISCUSS WHY WE LOG TRANSFORMED]


## Model Construction

<img src="./Images/model_vis.png" align="center"> <br>

The final model is an ensemble of nine indipendent models and was selected to prevent overfitting of a single model. Each model veries in its prediction, the ensemble takes the mean of the indipenent models output and outputs this means as the final prediction. The results observe a significant improvement of the ensemble models performance over any one of the indipendent models as demonstrated in the "Contributing Model Performance" section. We believe this is due to the different prediction each indipent model produced varried around the actual house price, and taking the average yielded a closer prediction more consistantly then any single model.

## Learnings
* Learnings


## Required Technologies
* Python 3.7
* Pandas
* Numpy
* XGBoost
* SkLearn
* MatPlotLib

## Future Work
1. Hypertuning each model
    *  There are opportunities to hypertune each model for better performance. Hypertuning each model will lead to a higher performing ensemble model. This includes normalizing and scaling data to exploring different combinations of attributes.
2. Further transformation study
    *  There are opportunities to investigate additional data transforms that may improve model performance. In addition, there are opportunities to explore the development of new attributes based of off existing attributes.
3. Data Processing - Nominal Data
    * We belive there are opportunities to develop ways to handel missing nominal data in a way that would boost model performance. This is an area we highly recommend exploring in future work.
4. Neighboorhood Assessment
    * Ames is a college town and such, certain neighboorhoods may have housing that is geared towards the college studend demographic. This insight may lead to further model development that captures this uniqness. It is worth further study.

## Credits
* Data Source: [Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)
* README template: [Cristopher Benge](https://cbenge509.github.io/) | [William Casey King, PhD](https://jackson.yale.edu/person/casey-king/) 
License
-------
<img align="right" width="250" src="./Images/datascience@berkeley.png"/>

Licensed under the MIT License. See [LICENSE](LICENSE.txt) file for more details.
