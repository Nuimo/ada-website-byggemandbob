
## Is success actually just explained by popularity? 
We now want to look at the effect the number of votes has on vote average and revenue. The vote  count of movies are distributed as a power law where some movies in our dataset has zero or very few votes and other movies have around 35 000 votes. Because of this we log-transform the vote count variable and plot this against the vote average and log-transformed revenue. 
As we can see on the two plots below the correlations between the independent variable and the dependent variables are positive and quite high. This suggests that as the number of votes increases, the average vote increases as well. Likewise, the plot showing log vote count vs log revenue shows a positive correlation. Here the correlation coefficient (r) and the coefficient of determination (R²) is higher indicating a stronger relationship. 

![Movie Vote count](figures/log_TMDB_vote_count/log_TMDB_vote_count_scatterplot.png){:width="80%"}