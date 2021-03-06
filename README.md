# Twist_Challenge_MOD.2

The goal of this project was to retrieve and clean a huge dataset, set up a database, apply a regression model, and build an interactive dashboard that shows the data and model. 

The challange selected for this project was to find a linear relationship between Years of Experience and Salary earned using a Linear Regression model from Scikit Learn. 

## Data

**source**: https://data.world/brandon-telle/2016-hacker-news-salary-survey-results
Data for this project was taken from Data World Opem Datasets, dowmloaded as a csv file and stored in a local directory. The Dataset is a result from a 2016 survey of Hacker News users about their salary and benefits.

### Preprocessing and cleaning

The data was preprocessed using both excel and postgresql. Excel because the raw data file had some data encoded in latin symbols and others the database could not read hence it was rejected.  In the excel file, the symbols had to be filtered out after which they were moved into the postgresql database. The skeletom for the table had tp be created using a query tool in postgresql after which the file was read directly from the local directory into the database using the query;

*COPY salaries FROM 'C:\Users\Nancy Armah\Desktop\Databases\salaries.csv' DELIMITER ',' CSV HEADER;*

Next the data in the data base was linked to jupyter notebook for further cleaning and preprocessing with the help of the following installations;
* !pip install ipython-sql
* !pip install sqlalchemy
* pip install psycopg2

**psycopg2** is used for PostgreSQL to enable us access the PostgreSQL database which contains our salaries.

The magic command **ipython-sql** enables us use of SQL magic functions that contains % and %% , allowing us to write SQL style code right in Jupyter Notebook.

After which the data goes through checks for empty cells, irrelevant columns are dropped and some created.

## Model

**Simple Linear Regression**

Simple linear regression is used to estimate the relationship between two quantitative variables. You can use simple linear regression when you want to know:

* How strong the relationship is between two variables (e.g. the relationship between salary and years of experience).
* The value of the dependent variable at a certain value of the independent variable.

The formula for a simple linear regression is:

        y=ax+b


b = slope  

a = intercept  

y = y- coordinate  

x = x-coordinate  

The correlation between total years experience and total compensation was 0.11. Even though there is a positive relationship between the two, the relationship is not a strong one per our data. 

After, the model is built by passing the x and y values through the regression model in sckit learn and our predicted values are generated.

## Building the Interactive DashBoard

The dashboard creation was the longest and most challenging part of this project. I started with PowerBi and Tableau but had to be dropped because of the difficulty in running a python script with the model in the app.

Finally settled on dash but it wasnt as interactive as id like because i spent too much time trying to figure powerbi and tableau out because i have experience using them.

Even though i have to submit this, i will keep working on the dashboard till i get it perfected and interractive.


