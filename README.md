# project1-group2

## Project Scope
### Our team will analyze IMDb’s API to parse out relevant data (e.g.,  revenue, genre, premier). After creating data frames using pandas in Jupyter Notebook, we will be able to visualize our data with matplotlib tools to better inform financial decisions. 

## Goals
### Creating a statistical analysis that provides predictions of which movies, studios, directors, and actors will lead to the most sales.

## Analysis of movies
### -Title of movie 
### -Actors
### -World sales
### -Directors
### -IMDB/Rotten Tomatoes score
### -Year
### -Studio
### -Rating
### -Genre 

## Null Hypothesis
### There is no correlation between a film's actors, genres, studio, and director and their impact on box office sales. 

## Questions / Conclusions

## What factors can lead to better sales?
### To answer this question, we chose to focus on the impact of film studios, directors, actors, movie reception, genres, and movie ratings on box office revenue.

## Which film studios/directors/actors have the best sales?
### Based on the data, the simple answer for which director, studio, and actor has the best sales reveals that Steven Spielberg as a director has made the most in sales out of the top 1000 highest-grossing films, the Studio with the most sales is Disney, and the actor with the highest sales figures is Robert Downey Jr. This conclusion is reached by calculating the sum of  gross global sales per person/company.
### However we can see by looking over the data in a few different ways that it isn’t so simple to identify best performance or consistency in such a straightforward manner. For example, Steven Spielberg has the greatest cumulative sales across all directors appearing on the dataset; and has the most films on the dataset, but when you look at his sales figures, they are not drastically more than other directors on the list and when you take the average gross sales across all films by a director Steven Spielberg loses out to many of the other directors. The Russo Brothers, directors of several movies in the Marvel Cinematic Universe are number two in cumulative gross sales, but only have four films that made the list, which puts them as the top earning directors in average gross sales per film.
### Similarly with the Studios we see that Warner Bros. has slightly more films that have made the top 1000 highest-grossing films of all time than Disney, the next studio with the most films on the list, but Disney’s sales approach $20,000,000,000 more than Warner Bros.. Additionally, with the actors we can see that Billy Zane has a lead against other actors if you look at the average gross sales of the films he has top billing on, but in the list he only has top billing in one film which is Titanic; and in general a number of the actors that appear in the top of the average grossing sales per film don’t show the same kind of results as the other charts.
### What all of these data anomalies in each category allude to is that there is likely going to be a far more complex set of circumstances that contribute to a movie’s success and that trying to boil it down with sales data isn’t going to give you a clear path or understanding in a film’s success. By getting more variation in data presentation of the same dataset when looking at the data slightly differently, we lose cohesion and certainty for what we should be taking away from the data; and if there is tunnel-vision on one factor you will likely end up missing information that would be impactful to the decisions you would make based on the results of the data.

## Does a movie’s reception impact the revenue?
### We visualized the ratings data in relation to sales worldwide. Critical reception was measured with rotten tomatoes and audience reception with IMDb.
### Both data sets required formatting. Because the data typed were not numeric in the case of rotten tomatoes a function was defined to loop through the the series and remove non numerics. For IMDb’s data a simple lambda statement was used to get a series of base 10 integers.
## Conclusion
### There seems to be no direct correlation between ratings and worldwide earnings.
### More research is need to understand the relation between critical scores and audience scores.

## What genres are the most successful?
### We determined that action and adventure appeared the most in the dataset of the highest grossing movies. We took a closer look at these genres by analyzing the sum and mean of their box office sales. Initially, we learned that Sci-Fi and Fantasy had a higher box office average, however the data was inconsistent as the line plot increased and decreased significantly from year to year. Furthermore, action and adventure had the highest sum box office, which emphasied earlier data that there were a higher number of these movies performing in the top films, and the line plot revealed a more consistent average from year to year. Therefore, adventure and action were the most successful and consistent genres to produce.
![alt text](https://github.com/edwardAugust/project1-group2/tree/main/Output#:~:text=yesterday-,barchartgenre.png,-completed%20code)

## Does movie rating affect sales?
### Throughout the analysis of the film rating we have come to the conclusion that most of the movies in the top 500 are PG-13. The data we have put together shows that PG-13 and G on average per rating earn the highest amount of money. This may be because family friendly films may appeal to a wider audience. There is no proven data that just because it is PG-13 it will earn more money than the other ratings as other rating types have ranked higher been placed on higher positions on the chart. Data could possibly be showing because there could be more PG-13 movies than any other type of movies made. A large dataset of most movies would be needed to confirm. We must accept the bill hypotheses with our current dataset.

## Data Sources
### csv data: Top 1000 Highest Grossing Movies
### https://www.kaggle.com/datasets/sanjeetsinghnaik/top-1000-highest-grossing-movies
### We used this data to pull the top 500 highest grossing movies.

### API: OMDB API
### https://www.omdbapi.com/
### We used this API to aggregate necessary data that was not included in the original csv file.

## Data Cleanup
### We had to reformat titles in the csv file to exclude the year at the end.
### We merged the Highest Grossing Movies dataset with the data we pulled from the OMDB API dataframe.
### Some of the information we pulled contained further lists that required us to delineating data into different columns.
#### After delineating columns, some of the data contained special characters, which we had to exclude in our final data frame.
### We had to reformat audience and critic scores to ensure they both displayed data on a 100 point scale.

## Limitations
### There were some factors that we were not able to pull when gather data such as movie budget and actor salaries.
### The OMDB API only allowed us 1000 requests per day, we we had to be very careful and selective with the data we wanted to search.
### The data from Highest Grossing Movies csv only included films up to January 2022.