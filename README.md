# Microsoft New Movie Studio

<!-- <img src="images/movie_studio.jpeg" alt="Drawing" style="width: 900px;"/> -->
![](images/movie_studio.jpeg)

## Overview

This notebook examines various movie databases that encompass data from thousands of movies. It focuses on movies released in the past 10 years to ensure the results would remain relevant, and to understand how what metrics generate profit rapidly. 

The analysis was centered on 3 main points:
- genre
- budget  
- actors 

By conducting a study of these data points, the aim is to provide valuable insights to help Microsoft's new movie studio focus on the main indicators of a movie's success.

Action movies generated the highest profit from 2010 to 2018 with over $8 billion generated. Adventure and Comedy are the 2nd and 3rd most profitable genres. <br>Making a combination of these 3 genres is the first recommendation.

Second, Comedy movies have a higher return on investment but generate less. Microsoft should make Comedy films at lower cost (median of \\$21 million budget) to generate profit and build resources to create less, but more profitable Action and Adventure movies - which require a median investment of \\$80 million. 
A very high correlation was found between a movie's budget and its profit, so costs should not be saved there. 

Finally, some actors were identified as generating the most profit in recent years - and having them starring in an action movie would most likely contribute to higher results. These include: Robert Downey Jr., Dwayne Johnson, Chris Evans.


## Business problem

The project's goal is to provide Microsoft's head of new movie studio with 3 recommendations for the new studio they are creating. The actionable insights are based on data on existing movies' performances by understanding which movies are doing best at the box office. Datasets are from Box Office Mojo, IMDb, Rotten Tomatoes, The Movie Database and The Numbers.

From this data, Pearson's correlation was calculated to review the relationship between a movie's runtime and its profit. Median of both runtime and ratings was calculated to understand the relative preference. Groupby was used to review the sum of profit by genre and by actor.



## Data 

The data used for this analysis, among the data provided were datasets from 
- IMDb
    - movie_basics: movie title, genres, release dates, runtime
    - principals: categorizes persons in movies based on their id, the movie id they had a role in and what role they had in the movie: director, actor, producer, writer, etc. 
    - persons: each person's name with their id, along with descriptive information about them: birth, death year and primary profession.
    
- The Numbers. <br>
The data represents all movies' key metrics of performance and descriptions

## Data Understanding and Methods

The key variable to determine a movie's success in this analysis is how much worldwide profit a movie made from box office. 
It is calculated by subtracting the budget from worldwide box office. 

A histogram of all movies' profit was drawn to understand what profit threshold determines whether a movie is considered successful, from its results. 
<br> The histogram is highly skewed to the left, indicating most movies either don't make profit or make up to $300 million. 
The number of movies reduces drastically from the $500 million profit mark, making it the threshold to define top performer movies to base the analysis on.


With the key variable and threshold determined 3 main attributes of a movie are evaluated to understand how they relate to a movie's success. 

1. Genre
2. Budget
3. Casting: actors and actresses

To measure these, the sum of profit by genre was calculated using groupby. 
Pearson's correlation method was used to evaluate whether how long a movie lasts impacts its profit. 
The median was calculated both for runtime and rating to have a comparison to base results to. 
A many to many relationship was established between four dataframes to calculate the sum of profit by actor. 



The number of movies reduces drastically from the $500 million profit mark, making it the threshold to define top performer movies to base the analysis on.



## Conclusions

### 1. Genre 
* The first recommendation is to produce Action movies - which have generated the most profit from 2010 to 2018. This genre created 82 billion dollars profit over these years: 45 billion more than the second most profitable genre: Adventure. Comedy movies would come third recommendation for movies' genre to ensure reaching the highest profits rapidly. 

<!-- <img src="images/profit_genres" alt="Drawing" style="width: 900px;"/> -->
![](images/profit_genres.jpeg)



### 2. Budget 
* The second recommendation is to highly invest in movies that are made. Microsoft should make Comedy films at lower cost (median of \\$21 million budget) to build a higher budget fund. This fund should be used to create less, but more profitable Action and Adventure movies - which require a median investment of \\$80 million. 

![](images/median_budget.jpeg)


### 3. Casting 

* The last recommendation is to pick actors carefully. A list of actors became notably famous in their genre and are linked to higher profits generated. Actors such as Robert Downey Jr., Dwayne Johnson, Chris Evans have starred in the most profitable movies and became icons for the Action, Adventure and Comedy movies and are more likely to arouse interest for the movies they are part of. Care should be exercised to ensure these actors are associated with the genre they are famous for. 
<!-- <img src="images/profit_actors" alt="Drawing" style="width: 900px;"/> -->
![](images/profit_actors.jpeg)

#### Limitations 

* The analysis was run on the years 2010 to 2018 and would be more precise if it included even more recent data
* Some of the movies were not matched with a genre due to title differences and higher precision would be gained by pairing movie_id rather than merging on movie titles
* The analysis is based on box office profits, which do not include all other more recent revenue generators such as streaming revenue and product placement. 

## Next Steps
Next steps would be to gather information on other sources of revenue from movies:
* streaming revenue 
    * https://www.businessofapps.com/data/video-streaming-app-market/ provides some of this information
* product placement


## For More Information 
See the full analysis and code in the [Jupyter Notebook](notebook.pdf) as well as summary in this [presentation](presentation.pdf).


For additional info, contact [Albane Colmenares](mailto:albane.colmenares@gmail.com?subject=[GitHub]%20Source%20Han%20Sans)

## Repository Structure
```

├── images
├── .gitignore
├── README.md
├── microsoft-movie-analysis.ipynb
├── presentation.pdf
└── notebook.pdf

```

