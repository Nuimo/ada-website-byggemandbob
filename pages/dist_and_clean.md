# Data cleaning

Taking a first look at the data set, we see that only around 10% of the movies have a box office revenue entry. Therefore we enrich the data set with TMDB data (<mark>kilde</mark>). The TMDB data gives us new attributes like revenue, original movie language and movie ranking, that might be interesting for out analysis. After enriching the data, <mark>12</mark>% of the movies have a box office revenue entry.

## Distribution of data

Before diving into the data, it needs to be cleaned. Some of the movies have a runtime of 10 hours, or an actor with the height of 3 meters. All of these unrealistic attributes is removed, before continuing with the data. After removing outliers, the distribution are as shown below.

![Character meta dataset before cleaning](figures/dist_and_clean/after_cleaning_character.png){:width="70%"}

![Character meta dataset before cleaning](figures/dist_and_clean/after_cleaning_movie.png){:width="80%"}

The figures below show the distribution of the numerical variables in the two dataset. Some are the variables also look very heavy-tailed and might need to be transformed. The two attributes **Movie box office revenue** and **TMDB_vote_count** (movie ranking) has a very skewed distribution. Therefore we transform this variable to make it normal distributed, as shown on the right.

![Movie box office revenue and TMDB_vote_count before and after log transformation](figures/dist_and_clean/log_transforms.png){:width="80%"}

## Inflation

However, the value of the US dollar is not the same in 2023 as it was over two hundred years ago. There we have to take inflation into account. The plot below shows the increase of revenue and value of the US dollar through the years. [https://www.officialdata.org/us/inflation/1800?amount=1]: URL "Inflation rate in the US from 1800 to 2023"

![Inflation of the US dollar's effect on revenue](figures/dist_and_clean/inflation_rate.png){:width="50%"}

The log Movie box office revenue before and after balancing can be seen in the plot below.

![Inflation of the US dollar's effect on revenue](figures/dist_and_clean/inflation_plots.png){:width="80%"}

After balancing the revenue attribute, we can now continue our analysis.