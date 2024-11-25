# QSS20-Group-Project-COVID
repo for our Final Project on the COVID-19 Twitter dataset

# Project Title: Tweet Sentiment Score During COVID-19 Pandemic Across Political Affiliation

## Description
This project focuses on a public Twitter dataset from the time of the pandemic, with the dataset’s observations representing users’ tweets pertaining to the topics regarding COVID-19. Our primary question investigates how a user’s sentiment score varies across several factors such as political affiliation, economic conditions, pandemic-related keywords, and other social and demographic markers.

Political affiliation was central to our study, given the significant role that partisan perspectives played in shaping public attitudes toward health measures, economic policies, and government interventions during the pandemic. Similarly, economic themes in tweets were explored to gauge public sentiment about financial stability and policy responses. Pandemic-related keywords further enabled a deeper analysis of how specific topics, such as vaccination, contact tracing, or the country’s ruler (e.g. the Biden administration in the United States during the peak time period of the virus) influenced sentiment trends.

In addition to these primary factors, we extended our analysis to include secondary components that might also affect sentiment. These included social markers such as the user’s verification status and the number of friends in their network. Furthermore, we also considered temporal trends based on tweet timestamps and geographical influences derived from the user's reported location of posting. The analysis acknowledged both the international nature of the dataset and the US-specific users. However, given that the majority of postings (observations in the dataset) originated in the United States, our project focused on those users. Altogether, the above mentioned variables provide a comprehensive view of the sentiment dynamics across a diverse population.

## Repo Structure
### [Code](https://github.com/jovana-nikitovic/QSS20-Group-Project-COVID/blob/main/code):
`code/` directory: Contains all the scripts used in this project. Clicking on each of the notebook names will lead you to them:
#### [00_mia.ipynb](https://github.com/jovana-nikitovic/QSS20-Group-Project-COVID/blob/main/code/00_mia.ipynb)
##### Takes in:
- The "econ_sample.pkl" pickle file
- This is the Public Tweet dataset of Twitter users' posts during the time of the COVID-19
- Furthermore, it is subsetted down to keywords pertaining to the economy, government, and institutional regulations that Professor Chang kindly shared with us
##### What it does:
- The notebook creates several bar graph, box plot, and KDE plot visualizations of sentiment score by political affiliation for statistically significant keywords.
- It calculates the mean average sentiment score by political affiliation for over 20 keywords and tests whether they are well-represented in the dataset.
- It utilizes multiple methods of statistical significance testing such as the Shapiro-Wilk test, Levene’s test for equal variances, the Kruskal-Wallis test, and the Tukey Honest Significant Difference Test to evaluate the robustness of certain keywords (using 5% or 10% significance levels).

##### Outputs:
- Visualizations described in the Outputs section of this repo and the results of several statistical significance tests.

#### [01_alexa.ipynb](https://github.com/jovana-nikitovic/QSS20-Group-Project-COVID/blob/main/code/01_alexa.ipynb)
#### Takes in: 
- The "econ_sample.pkl" pickle file
- This is the Public Tweet dataset of Twitter users' posts during the time of the COVID-19
- Furthermore, it is subsetted down to keywords pertaining to the economy, government, and institutional regulations that Professor Chang kindly shared with us
#### What it does:
- This notebook creates a new column called "political_affil" that designate each state to the political party (Republican (Red), Democrat (Blue), and Flip (Purple)) they had a majority of in the 2020 election.
- It creates a new dataframe for each graph that selects five states with the most tweets from each political party.
- It creates line graphs that chart the change in sentiment score over time of respective keywords from tweets from each political party's top five states.
- On each graph it adds annotations that include important information regarding events that were relevant at that point in time.
#### Outputs:
- Line graphs that display the change in sentiment score regarding certain keywords over time for the three political parties, and includes annotations that refer to current events of the time.

#### [02_jovana.ipynb](https://github.com/jovana-nikitovic/QSS20-Group-Project-COVID/blob/main/code/02_jovana.ipynb)
##### Takes in:
- The "econ_sample.pkl" pickle file
- This is the Public Tweet dataset of Twitter users' posts during the time of the COVID-19
- Furthermore, it is subsetted down to keywords pertaining to the economy, government, and institutional regulations that Professor Chang kindly shared with us
##### What it does:
- The notebook creates Summary Graphics Visualizations of geographic variations in setiment score: International (Country-based) and US-specific (further broken down by the Political Affiliation Category)
- It performs three iterations of Linear Regression where sentiment score is being predicted based on social markers of Twitter users displayed publicly
- It performs two Multinomial Logistic Regressions, where the target variable (political affiliation) differs in terms of classes: four ("Red", "Blue", "Flip", "Unknown") vs three (without the "Unknown", which turned out to be the majority class)
##### Outputs:
- Visualizations described in the Outputs section of this repo, as well as the evaluations of the models



### [Output](https://github.com/jovana-nikitovic/QSS20-Group-Project-COVID/blob/main/output):
`output/` directory: Holds graphs and figures generated by the scripts. Clicking on each of the folder names will lead you to these directories:
#### [00_outputs_mias_topic](https://github.com/jovana-nikitovic/QSS20-Group-Project-COVID/blob/main/output/00_outputs_mias_topic)
- file 00_vaccination_avg.png is a bar graph reflecting various sentiment scores by political affiliation for the key word "vaccination"
- file 01_vaccination_distrib.png reflects the sentiment score distribution by political affiliation for the key word "vaccination"
- file 02_vaccination_kde.png is a kde plot reflecting various sentiment scores by political affiliation for the key word "vaccination"
- file 03_vaccination_tukey reflects the results of several significance tests on our findings for the key word "vaccination"
- file 04_lockdown_avg.png is a bar graph reflecting various sentiment scores by political affiliation for the key word "covid lockdown"
- file 05_lockdown_distrib.png reflects the sentiment score distribution by political affiliation for the key word "covid lockdown"
- file 06_lockdown_kde.png is a kde plot reflecting various sentiment scores by political affiliation for the key word "covid lockdown"
- file 07_lockdown_tukey reflects the results of several significance tests on our findings for the key word "covid lockdown"
- file 08_tracing_avg.png is a bar graph reflecting various sentiment scores by political affiliation for the key word "contact tracing"
- file 09_tracing_distrib.png reflects the sentiment score distribution by political affiliation for the key word "contact tracing"
- file 10_tracing_kde.png is a kde plot reflecting various sentiment scores by political affiliation for the key word "contact tracing"
- file 11_tracing_tukey reflects the results of several significance tests on our findings for the key word "contact tracing"
- file 12_biden_avg.png is a bar graph reflecting various sentiment scores by political affiliation for the key word "biden"
- file 13_biden_distrib.png reflects the sentiment score distribution by political affiliation for the key word "biden"
- file 14_biden_kde.png is a kde plot reflecting various sentiment scores by political affiliation for the key word "biden"
- file 15_biden_tukey reflects the results of several significance tests on our findings for the key word "biden"

#### [01_outputs_alexas_topic](https://github.com/jovana-nikitovic/QSS20-Group-Project-COVID/blob/main/output/01_outputs_alexas_topic)
- file 00_sentiment_analysis_overall.png is a line graph over months that illustrates the change in sentiment of all tweets with relevant keywords across political affiliation
- file 01_sentiment_analysis_biden.png is a line graph over months that illustrates the change in sentiment of all tweets with the keyword "biden" across political affiliation. The graph also includes annotations that mention relevant events.
- file 02_sentiment_analysis_vaccination.png is a line graph over months that illustrates the change in sentiment of all tweets with the keyword "vaccination" across political affiliation. The graph also includes annotations that mention relevant events.
- file 03_sentiment_analysis_stimulus.png is a line graph over months that illustrates the change in sentiment of all tweets with the keyword "stimulus" across political affiliation. The graph also includes annotations that mention relevant events.

#### [02_outputs_jovanas_topic](https://github.com/jovana-nikitovic/QSS20-Group-Project-COVID/blob/main/output/02_outputs_jovanas_topic)
- file 00_international_sent.png contains the visualization for the International Sentiment Score ~ Bottom 10 and Top 10
- file 01_us_sent_political.png contains the visualization for the US Sentiment by Political Affiliation ~ Bottom and Top Score
- file 02_friends_verification_sent.png contains the visualization for the Sentiment Score based on Friends Count and User Verification Status
- file 03_verification_political_distr.png contains the visualization for the Distribution of Political Affiliation based on User Verification Status
- file 04_friends_political_distr_box.png contains the visualization for the Distribution of Friends Count based on Political Affiliation
- file 05_linear_regressions.png contains the table for the three Linear Regressions (univatiate, bivariate, and bivariate where the continuous feature is log-normalized), listed in terms of predictive performance
- file 06_logistic_regressions.png contains the table for the two Multinominal Logistic Regressions, differing in terms of the response variable (four categories versus three categories in the prediction)
- file 07_logistic1_confusion_mat.png contains the Confusion Matrix for Logistic Regression 1 (4 categories)
- file 08_logistic1_class_rep.png contains the Classification Report for Logistic Regression 1 (4 categories)
- file 09_logistic2_confusion_mat.png contains the Confusion Matrix for Logistic Regression 2 (3 categories)
- file 10_logistic2_class_rep.png contains the Classification Report for Logistic Regression 2 (3 categories)

## Data Storage
The data for this project is stored in this cloud folder: https://drive.google.com/drive/u/0/folders/1ACR_1iMMNfYeT77auRCKCw14l_EnXKbc
Professor Chang shared these datasets with us. Thank you so much!
We focused mainly on the dataset named "econ_sample.pkl", as well as the US-electoral data of presidential results in 2020 from the following website: https://www.cnn.com/election/2020/results/president

