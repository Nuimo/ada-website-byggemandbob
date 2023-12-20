## Dataset description
First of all the dataset we are using is the 
CMU Movie Summary Corpus and TMDB.
Secondly, before starting to analyse the data, it is important to actually understand what each column name represents and what the importance of it is. Here we are going to create a table that gives a nice overview of the different columns name.

Importantly we are only going to mention the significant ones and the ones that need some explanation - the full list can be found below by toggling the collapsible section "Details".

| Column Name                                  | Data Type | Description                                        |
|----------------------------------------------|-----------|----------------------------------------------------|
| Movie runtime                                | Float     | Duration of the movie in minutes                   |
| Movie languages                              | String    | Languages the movie has been released in           |
| Movie countries                              | String    | Countries where the movie was produced             |
| TMDB_original_language                       | String    | Original language of the movie as per TMDb         |
| TMDB_vote_average                            | Float     | Average rating for the movie from TMDb             |
| TMDB_vote_count                              | Float     | Number of votes the movie received on TMDb         |
| Movie box office revenue                     | Float     | Box office revenue of the movie                    |

### All Dataset Columns
<details markdown="1">

| Column Name                                  | Data Type | Description                                        |
|----------------------------------------------|-----------|----------------------------------------------------|
| Wikipedia Movie ID                           | Integer   | Wikipedia's unique identifier for the movie        |
| Freebase Movie ID                            | String    | Freebase's unique identifier for the movie         |
| Movie release date                           | String    | The release date of the movie                      |
| Movie runtime                                | Float     | Duration of the movie in minutes                   |
| Movie languages                              | String    | Languages the movie has been released in           |
| Movie countries                              | String    | Countries where the movie was produced             |
| Movie genres                                 | String    | Genres associated with the movie                   |
| TMDB_id                                      | Float     | The Movie Database (TMDb) unique identifier        |
| TMDB_original_language                       | String    | Original language of the movie as per TMDb         |
| TMDB_original_title                          | String    | Original title of the movie as per TMDb            |
| TMDB_overview                                | String    | Overview or summary of the movie as per TMDb       |
| TMDB_popularity                              | Float     | Popularity score of the movie as per TMDb          |
| TMDB_release_date                            | String    | Release date of the movie as per TMDb              |
| TMDB_title                                   | String    | Title of the movie as per TMDb                     |
| TMDB_vote_average                            | Float     | Average rating for the movie from TMDb             |
| TMDB_vote_count                              | Float     | Number of votes the movie received on TMDb         |
| TMDB_runtime                                 | Float     | Runtime of the movie as per TMDb                   |
| TMDB_budget                                  | Float     | Budget of the movie as per TMDb                    |
| TMDB_IMDB_id                                 | String    | IMDb's unique identifier for the movie             |
| TMDB_genres                                  | String    | Genres of the movie according to TMDb              |
| Movie box office revenue                     | Float     | Box office revenue of the movie                    |
| Movie release year                           | Float     | Year of the movie's release                        |
| log Movie box office revenue                 | Float     | Logarithm of the movie's box office revenue        |
| log TMDB_vote_count                          | Float     | Logarithm of the number of TMDb votes              |
| Male_actor_percentage                        | Float     | Percentage of male actors in the movie             |
| Mean_actor_age_at_movie_release              | Float     | Average age of actors at the time of movie release |
| balanced Movie box office revenue            | Float     | Balanced box office revenue of the movie           |
| log balanced Movie box office revenue        | Float     | Logarithm of balanced box office revenue           |



</details>


Taking a first look at the data set, we see that only around 10% of the movies have a box office revenue entry. Therefore, we enrich the data set with TMDB data  ([TMDB](https://www.themoviedb.org)). The TMDB data gives us new attributes like revenue, original movie language and movie rating, that might be interesting for our analysis. After enriching the data, 12% of the movies now have a box office revenue entry.

