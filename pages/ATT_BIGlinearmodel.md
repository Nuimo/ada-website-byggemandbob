## Big linear model
(stikords agtigt skrevet, note: brug peter på plots til hjælp med at beskrive dm hvis d er)

now want to investigate how the different traditional attributes contribute to high revenue and rating.

we do this by creating two linear regression model predicting revenue and rating based on traditional variables (figures: BOBsYndlingsPlot, maybe also Correlation_matrix_numerical_variables)
Only relevant predictor variables chosen.

Inspected predictor relevant variables, pairwise correlation and distribution, want to avoid multicollinearity

categorical variables with multiple values per element: Movie_countries and Movie_genres


Computational expensive: One-hot-encoding for top 10 most occuring values in both variables (maybe visualize with the barplots)

linear regression models with all the same predictor variables but different target variables: revenue and regression

predictor variables: original_language + Movie_runtime + Movie_release_year + log_vote_count + Male_actor_percentage + Mean_actor_age + Movie_countries + Movie_genres

target variables: log_revenue for model1 and avg_rating for model 2

R^2 value: around 0.4-0.45 for both models, not a lot of variance is explained with this type of model = not the most fitting model for our data.

We now want to look at how the significant coefficients affects our target variables: (coefficient plots)
interpret these plots: The top 5 strongest positive and negative coefficients for model1 and model2, are they different or the same?


#### transitioning to NLP model and stuff:
Traditional attributes are not very telling about the movie as they only provide some general movie info and not a lot of details that can reveal the story.
plot summaries: more specific to the movie, more complex and contains more details about the movies. More distinct features.


