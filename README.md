# WHAT-MAKES-A-MOVIE-SUCCESSFUL-
Looking into factors that affect a movies success in the box office using moive_metadata dataset. 

Initial dataset inspection and cleaning carried out in python. 

# RESULTS FROM EDA 

To run this section, download 'movie_metadata' and copy code from 'EDA_CODE' file into google collab.

The uncleaned dataset is found to have 45466 observations and 24 variables. 

## DATA TYPES 
19 of the varibles have datatype 'object' , suggesting text values . 5 vairbles have data type 'float 64' suggesting decimal numbers. 

## MISSING VALUES

## Missing Values Summary

The below tables shows the missing values of each variable, with some containing a majority of missing values. 

| Variable              | Missing Count | Missing (%) |
| --------------------- | ------------: | ----------: |
| belongs_to_collection |        40,972 |      90.12% |
| homepage              |        37,684 |      82.88% |
| tagline               |        25,056 |      55.11% |
| overview              |           954 |       2.10% |
| poster_path           |           386 |       0.85% |
| runtime               |           263 |       0.58% |
| release_date          |            87 |       0.19% |
| status                |            87 |       0.19% |
| imdb_id               |            17 |       0.04% |
| original_language     |            11 |       0.02% |
| revenue               |             6 |       0.01% |
| title                 |             6 |       0.01% |
| video                 |             6 |       0.01% |
| vote_average          |             6 |       0.01% |
| spoken_languages      |             6 |       0.01% |
| vote_count            |             6 |       0.01% |
| popularity            |             5 |       0.01% |
| production_companies  |             3 |       0.01% |
| production_countries  |             3 |       0.01% |

There are 17 duplicate rows within the dataset 

## Summary Statistics (Numeric Variables)

The table below shows the summary statistics for the numerical variables. Looking to the means and medians gives a brief insight to the normality of the variables, with some such as revenue seeming highly un-normal and others such as runtime seeming normal. Further investigation must take place to properly determine this. 
| Statistic          |       Revenue | Runtime |  Video | Vote Average | Vote Count |
| ------------------ | ------------: | ------: | -----: | -----------: | ---------: |
| Count              |        45,460 |  45,203 | 45,460 |       45,460 |     45,460 |
| Mean               |    11,209,350 |   94.13 |  0.002 |         5.62 |     109.90 |
| Standard Deviation |    64,332,250 |   38.41 |  0.045 |         1.92 |     491.31 |
| Minimum            |             0 |       0 |      0 |         0.00 |          0 |
| 25th Percentile    |             0 |      85 |      0 |         5.00 |          3 |
| Median (50%)       |             0 |      95 |      0 |         6.00 |         10 |
| 75th Percentile    |             0 |     107 |      0 |         6.80 |         34 |
| Maximum            | 2,787,965,087 |   1,256 |      1 |        10.00 |     14,075 |

# CLEANING THE DATA

## removal of duplicates 

the removal of duplicates has resulted in a new observation count of 45499 

## Removal of variables

EDA has revealed some of the variables to contain a majority of missing values or the same value, resulting in low explanatory power. As a result these variables are removed. 

to begin with unnamed columns were removed. 24 variables remain, suggesting this is not an issue. 


## coversion of variables


the variables look numerical however the results of EDA produced text values (object). As a result these variables must be fixed, with any non-numrical inputs being coverted into missing values. 

## Missing values

To explore missing values, look back to the initial table in EDA section. The main approach used in removing missing data was to remove any observations missing multiple values in key variables, such as Title and popularity. 

# Removal of variables
Another factor that aids the removal of missing values is the exploration of the variables. EDA showed some of the variables contained majority missing values. Choosing a threshold of 70% missing values , majority missing value variables were removed, resulting in the removal of variables 'belongs_to_collection' and 'homepage' .     

#SQL work 

Researched and built skills in SQL to continue analysis
