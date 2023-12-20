# Data cleaning

Before diving into the data, it needs to be cleaned. Some of the movies have a runtime of 10 hours, or an actor with a height of 3 meters. All of these unrealistic attributes are removed, before continuing with the data. After removing outliers, the distributions are as shown below.

![Character meta dataset before cleaning](figures/dist_and_clean/after_cleaning_character.png){:width="80%"}

![Character meta dataset before cleaning](figures/dist_and_clean/after_cleaning_movie.png){:width="90%"}

The figures below show the distribution of the numerical variables in the two datasets. Some of the variables also look very heavy-tailed and might need to be transformed. The two attributes **Movie box office revenue** and **TMDB_vote_count** (movie rating) has a very skewed distribution. Therefore, we transform this variable to make it normal distributed, as shown on the right.

![Movie box office revenue and TMDB_vote_count before and after log transformation](figures/dist_and_clean/log_transforms.png){:width="80%"}

## But what about inflation?

However, the value of the US dollar is not the same in 2023 as it was over two hundred years ago. Therefore, we have to take inflation into account. The plot below shows the increase of revenue and value of the US dollar throughout the years. ("Inflation rate in the US from 1800 to 2023" [OfficialData](https://www.officialdata.org/us/inflation/1800?amount=1))

![Inflation of the US dollar's effect on revenue](figures/dist_and_clean/inflation_rate.png){:width="50%"}

The log Movie box office revenue before and after balancing can be seen in the plot below.

![Inflation of the US dollar's effect on revenue](figures/dist_and_clean/inflation_plots.png){:width="90%"}

After balancing the revenue attribute, we can now continue our analysis.