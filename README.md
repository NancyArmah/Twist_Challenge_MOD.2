# Twist_Challenge_MOD.2

The goal of this project was to retrieve and clean a huge dataset, set up a database, apply a regression model, and build an interactive dashboard that shows the data and model. 

The challange selected for this project was to find a linear relationship between Years of Experience and Salary earned using a Linear Regression model from Scikit Learn. 

## Data

**source**: https://data.world/brandon-telle/2016-hacker-news-salary-survey-results
Data for this project was taken from Data World Opem Datasets, dowmloaded as a csv file and stored in a local directory. The Dataset is a result from a 2016 survey of Hacker News users about their salary and benefits.

### Preprocessing and cleaning

The data was preprocessed using both excel and postgresql. Excel because the raw data file had some data encoded in latin symbols and others the database could not read hence it was rejected.  In the excel file, the symbols had to be filtered out after which they were moved into the postgresql database. The skeletom for the table had tp be created using a query tool in postgresql after which the file was read directly from the local directory into the database using the query;

COPY salaries FROM 'C:\Users\Nancy Armah\Desktop\Databases\salaries.csv' DELIMITER ',' CSV HEADER;

Next the data in the data base was linked to jupyter notebook for further cleaning and preprocessing with the help of the following installations;
* !pip install ipython-sql
* !pip install sqlalchemy
* pip install psycopg2

