compared to other IDE's like spyder and pycharm Jupyter notebook is easy to use


LIFE CYCLE OF DATA SCIENCE.... 7 steps are mandatory

1. Business understanding
2. Data collection
3. Data Cleaning
4. Data Analysis
5. Feature Engineering
6. Model Building
7. Deployment

1----Business Understanding:

Client/product owner/domain experts -----> comes with a project and converse with Business Analyst----->try writing requirements of that particular requirements ------> these requirements are sent to data analyst/data scientist----->business analyst(will decide from where we can extract data, data available is 1)live streaming 2)3rd party apis 3)comapny Db or 4)specialised Db)

2----

Data collection:
 could be CSV...comma seperated values
          TSV...tab seperated values
          JSON....Javascript object Notation...Key value pairs
          datawarehouses
          databases---> 2 catogeries ----
sql data bases(store data in tables(rows and columns)---so called table centric databases
No SQL database....data stored in document...so document centric
Specialised database----> Hive(hiveQL), Hadoop, Spark(SparkQL)

As soon as we do data collection... it is called RAW DATA( which consists of typos, errors, and looks messy)

SO we have to do Data Cleaning:

remove duplicate entries in data
remove irrelavant rows
remove missing values
Fix datatype of all the features

More the data is RAW...more data cleaning is necessary


DATA CLEANING/DATA WRANGLING/ DATA PRE-PROCESSING----synonymns


4.....Data Analysis/ Exploratory Data Analysis


before building model....first understand the model

predict--->what could be prices of airlines...for that what are different airlines---generating high revenue, having high rush etc.



Feature Engineering--->examine and convert each and every feature of model in such a way that model/algorithm can accept that


Feature engg is a broad area.
Example: Imagine predict prices of airline..
tell me departure city, arrival city, times, total passengers

Suppose we have 10 Million data points out of which upto 8 Million prices are present.
can you predict for the rest of entries??? NO it's a string...air asia is a string

You need data in the form of number or Vector
Data science---> Math
In a nutshell it is called Feature Encoding(convert string into numbers)-----Catogerial Features into numbers

imagine there are 500 columns...of which all aren't important
                   Model Building
                   Subset
                   Feature Selection
                   Feature scaling/transformation/Feature Normalization
Outlieres----- either extremely high or very low values is called outliers
Dimentionality Reduction--->if data is in very high dimentional space

From DATA COLLECTION to FEATURE ENGINEERING steps it is called ETL Pipeline(Extract data
Transform data, Load Data)

output of ETL pipeline is all about From Raw data to Featurized data
that featurized data is sent to Model building
E- extract data - > we get Raw Data
T - Transform data - > Data cleaning + Featuring Engineering
L - Load Data      - > Export data, do data analysis and send it to model building

Model Building 

Building model using featured data is cake walk...just takes 50-100 lines

Featurized data -to--- Model Building

example consider the Make my trip app....asks the source city, destination city and route consider...now the price of airline has to be predicted....for an end user we take all of this...simply this is DEPLOYMENT.

Data Science Applications:

1. Ola/Uber---particular driver reaches the place in given time
2. Google Maps ---> you'll be reaching to destination in particular amount of time.
3. Amazon and Netflix----> Recommendations like new series, products