# QSS20-Group-Project-COVID
repo for our Final Project on the COVID-19 dataset

# Project Title: Our Title

## Description
We’d like to investigate the relationship between an increase in COVID-19 cases and an increase in Tweets professing a negative sentiment towards the government. We want to further examine this potential relationship between “red” and “blue” states. Our Null Hypothesis is that, with the increase in COVID-19 reported cases, the number of tweets professing a negative perspective towards the government would increase at a higher rate in “red” states than it would in “blue” states.

## Repo Structure
### Code:
`code/` directory: Contains all the scripts used in this project.

### Output:
`output/` directory: Holds graphs and figures generated by the scripts.
#### 02_outputs_jovanas_topic
- [00_international_sent.png](https://github.com/jovana-nikitovic/QSS20-Group-Project-COVID/blob/main/output/02_outputs_jovanas_topic/00_international_sent.png) 
- file 00_international_sent.png contains the visualization for the International Sentiment Score ~ Bottom 10 and Top 10
- file 01_us_sent_political.png contains the visualization for the US Sentiment by Political Affiliation ~ Bottom and Top Score
- file 02_friends_verification_sent.png contains the visualization for the Sentiment Score based on Friends Count and User Verification Status
- file 03_verification_political_distr.png contains the visualization for the Distribution of Political Affiliation based on User Verification Status
- file 04_friends_political_distr_box.png contains the visualization for the Distribution of Friends Count based on Political Affiliation
- file 05_linear_regressions.png contains the table for the three Linear Regressions (univatiate, bivariate, and bivariate where the continuous feature is log-normalized), listed in terms of predictive performance
- file 06_logistic_regressions.png contains the table for the two Multinominal Logistic Regressions, differing in terms of the response variable (four categories versus three categories in the prediction)
- file 07_confusion_mat_logistic.png contains the two tables displaying Confusion Matrices for each of the abovementioned Multinominal Logistic Regressions (in order to display class imbalance for the first model and demonstrate how looking at the accuracy measure alone can be misleading without looking at the accompanying Macro Avg. and Weighted Avg. metrics)

## Data Storage
The data for this project is stored in this cloud folder: https://drive.google.com/drive/u/0/folders/1ACR_1iMMNfYeT77auRCKCw14l_EnXKbc
Professor Chang shared the dataset with us. Thank you so much!

