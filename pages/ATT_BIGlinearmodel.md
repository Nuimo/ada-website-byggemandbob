## Connecting the dots - can we make one big linear model? 

We now want to investigate how the different attributes in our dataset contribute to a high revenue and rating.

We do this by creating two linear regression model predicting revenue and rating based on basic attributes of the movies. We were able to include the following numerical attributes in our models: Movie runtime, Movie release year, Vote count, Male actor percentage, and Mean actor age. We did this in order to only include relevant predictor variables. 

In order to get an overview of the pairwise correlation between the different numerical variables of our model, we created the correlation and pairs plot displayed below. The plot the displays the coefficient of correlation of every variable against all other variables in the upper right side of the diagonal. The diagonal of the plot shows a histogram of the variables. Lastly, the lower left half of the plot shows scatter plots of the different variables against each other together with the linear regression line of the data. With this plot the relevant predictor variables can be inspected in terms of the pairwise correlations and distributions. 

We want to avoid multicollinearity in our model, and therefore it is crucial that the independent variables remain uncorrelated. Otherwise the integrity of our model's predictions can be questioned. As observed in the plot, while certain variables show a tendency to correlate, such as the 'TMDB vote count' and 'Movie revenue' with a correlation coefficient of 0.57 suggesting a moderate positive relationship, other variables demonstrate weaker correlations. This can be seen from the close to horizontal trend lines and small correlation coefficients. 


![BOBsYndlingsPlot](figures/Big_linear_model/BOBsYndlingsPlot.png){:width="80%"}

We also want to add some categorical attributes to our model: Movie country, Movie language, and Movie genre. These categorical variables have a lot of different entries and it would therefore be very computationally expensive to include all countries, languages and genres of our dataset. Therefore, we one-hot-encode the top 10 most occuring values of the variables. 

Having stated all our independent variables to our models we can now formulate our linear regression models. The two models describing the vote average and revenue have the same predictor variables but different target variables as seen below:

**Predictor variables:** 
C(Original_language) + Movie_runtime + Movie_release_year + log_vote_count + Male_actor_percentage + Mean_actor_age + C(Movie_countries) + C(Movie_genres)

**Target variables:** 
Model1: Log_revenue
Model2: Avg_rating

The R-squared value is 0.452 for the revenue model and 0.402 for the average rating model. This means that  approximately 45.2% and 40.2% of the variability in movie revenues and TMDB vote average can be explained by the model's variables. This is a moderate level of explanatory power. The models also have significant F-statistics, indicating that the variables, as a group, have a statistically significant effect on movie revenues.

#### Can we still draw some insights from this model?
Even though the overall fit of our model is not great we can still look at which variables shows the highest impact on our target variables. The coefficient plots below show the significant coefficients in our two models sorted after coefficient value.  Variables with bars extending right have a positive effect, while those extending left have a negative effect on average ratings. The length of each bar indicates the strength of the variable's impact within a statistical significance of p-value < 0.05.

![Coefficient_rating_mode](figures/Big_linear_model/Coefficients_rating_model.png){:width="80%"}

The plot above shows the coefficients for the linear regression model on movie ratings. We can see that certain genres such as Family and Action positively influence ratings. The same is evident for certain production countries and languages.

![coefficient_revenue_model](figures/Big_linear_model/Coefficients_revenue_model.png){:width="80%"}

The revenue coefficient plot above has a number of positive coefficients.  The top 10 genre's or country's positively impact revenue. Family films and movies from the United States show the strongest positive relationships. In contrast, South Korean productions and the Adventure genre show a negative correlation with revenue. Non-categorical variables like 'log_TMDB_vote_count' significantly influence revenue, indicating a robust relationship between a film's popularity and its financial success.

Finally, we can conclude that categorical variables of the 10 most evident genres, contries and languages show a higher influence on the model than the non-categorical variables. 


#### How can we move to better models?
The attributes associated with our dataset do not explain a large percentage of the variance or our data. A reason that this somewhat simple linear regression cannot easily predict movie success in terms of revenue or rating could be because these models only provide general information about the movies and not specific details of the storyline of the movies. 
We therefore want to investigate whether knowing the specific storyline of each movie can help us in predicting movie success. As plot summaries are more complex and contain more specific details about the movies we can maybe extract more distinct features from our dataset. This leads us to the next part of our analysis where we will try to cluster movies into distinct categories based on their respective plot summaries. 


