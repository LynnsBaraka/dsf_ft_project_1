# Movie Studio Genre Recommendation

## Project Goal

The project aim is to find out the preferred movie genres 

## Data sources and exploration

The data sources used in this analysis were extracted from the cloned project 1 repository on github. 

A total of 3 dataframes were used: The gross movies csv file and the movie ratings and movie basics data frames obtained from the im.db database file. 

## Overview

#### Background of the business.
Microsoft is a leading global brand in creating household and business software solutions as well as hardwaresuch as laptops. 

### Domain of the business.
The film industry represents a captivating realm that spans from the creation and distribution of cinematic content to its presentation on the big screen. It's a fusion of artistic narrative, cutting-edge technology, and societal trends, constantly evolving at the crossroads of creativity and commerce.

### Business case
Microsoft, a leading global brand, wants to venture into the movie production industry. They want to create a new movie studio and need to know the types of films that are currently doing well in the entertainment industry. 

### Business Understanding
Objectives
The objectives of the project are: 

* To find the most preferable movie durations
* To find out the best performing genres types of films
* To find out the best markets to tap into to maximize profitab
* To generate actionable information on what Microsof can capitalize on. 

### Data Understanding

* The movie gross data frame had a total of 5 columns: 
* Title - The movie title. 
* Studio - The production studio name 
* Domestic_gross - The amount of money the film earned in the US
* Foreign_gross- The amount of money the film earned in the rest of the world.
* Year- The year the film was produced. 

The movie basics table had 6 columns: 
* Movie id - a unique code to identify each movie
* Primary title - The primary title of the movie
* Original title - The original movie title
* Start year - The year the movie was released
* Runtime_minutes - The movie duration
* Genres - The movie genre
* The movie ratings table had 3 columns:
* Movie id - a unique code to identify each movie
* Average rating - the average rating of the movie
* Numvotes - The number of votes that the movie got. 

It was noted that the movie ratings and movie basics dataframes each had the movie id column which was used to identify each movie. It was therefore a common characteristic that was used to relate the two tables. 

## Data cleaning.
The data frames were found to have missing values, wrong data types in the columns and abnormal readings in the statistical summaries.

The null value percentages wre calculated and dropped accordingly. For numerical values, their data types were changed from string objects to float type as they were in hundreds of millions and billions. 

Abnormal values such as 3 minute movies and 5,000 minute movies were trimmed away. 
White spaces that could compromise the visualization process were also truncated. 

The tables movie ratings and movie basics tables were joined on the movie id column since it was a common column in both data frames. 

## Exploratory Data  Analysis

### Univariate analysis
The characteristics of the individual variables domestic gross, foreign gross, studios, runtime and average ratings were done. 
The statistical counts, maximum and minimum were calculated. 

### Bivariate analysis

Two related variables were studied to find correlations. The following comparisons were made: 
* Movie runtime and number of votes
* Genre and average rating
* Genre and number of votes
* Gross domestic returns and studio
* Gross foreign returns and studio

### Multivariate analysis
Movie studios, years of production, gross foreign and gross domestic returns were compared. 

### Plots
The following libraries were used for visualization: 
* Matplotlib
* seaborn
* plotly

A scatterplot of the runtime against the number of votes was visualized. The visualization showed a higher concentration of number of votes with movies between 90 and 150 minutes.

The top 10 genres according to average rating were plotted against the total votes on a bar chart. It was visualized that genre combinations of Action, Adventure, Scifi and Action, Adventure, Fantasy got the highest number of votes.

A line chart of the top movie studios, their domestic gross and foreign gross over the years revealed that their returns were more in te foreign market than in the domestic market. 

Recommendations
1. Microsoft should make movies that are of medium length, between 90 and 150 minutes as they receive the highest number of votes. 

2. They should consider mixing genres in their movie production, specifically action with adventure and Sci-Fi or Fantasy as the two combinations are the most popular according to the average movie rating.

3. They need to tap into the foreign market more than the domestic market since trends show that the most successful movie studios generate more revenue from the foreign markets. 


### Next Steps
More geographical data is required so as to compare different movie ratings in different regions of the world, to give more detailed insights instead of generalizing the entire foreign market. 
