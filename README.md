
# Amazon_Vine_Analysis

Performing ETL and Analysis on Amazon Product Reviews to determine bias of favorable VINE reviews. 

## Overview 
The purpose of this project is to analyze Amazon product reviews and uncover favorability of Vine program reviews over regular reviews.
In order to analyze and uncover any insights a large amount of review data must be processed. 

## Database Schema 
In order to properly process and analyze the review data, I have created a database schema within AWS to load the data into once it is transformed. 


## ETL Process 

Pyspark is first used to extract and read in review data from an Amazon S3 Data storage server. 

Pyspark is then used to transform the data by creating Dataframes from subsets, which will match the tables within the database and schema constraints. 



After creating the dataframes, they are loaded into the database.


## Querying Database 

With the data loaded, it is now possible to efficiently traverse and perform analysis. 
In order to gain a more granular understanding of the review data, additional tables are created within the database through several queries. 



## Analyzing with Pandas  
With even more focussed subsets of review data created within the database, analysis is smoothly performed with pandas in python by connecting my environment to the database and loading the needed tables.

## Summary 

Based on the data summary, there is not sufficient evidence of there being any positivity bias for reviews in the Vine program. 
Since there is roughly the same percentage of 5 star rated reviews for vine and non-vine reviews, one is not shown to be proportionately favored over the other. 

## Further Analysis 
To further delve into the topic of positivity bias, a further analysis on customer votes can be performed. In Which the ratio of "helpful_votes'” can be reviewed, as well as using "verified_purchase" as threshold. 


