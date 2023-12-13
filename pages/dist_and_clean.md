---
layout: default
---

# Data cleaning

Taking a first look at the data set, we see that only around 10% of the movies have a box office revenue entry. Therefore we enrich the data set with TMDB data (<mark>kilde</mark>). The TMDB data gives us new attributes like revenue, original movie language and movie ranking, that might be interesting for out analysis. After enriching the data, <mark>hvor meget??</mark>% of the movies have a box office revenue entry.

## Distribution of data

Before diving into the data, it needs to be cleaned. Some of the movies have a runtime of 10 hours, or an actor with the height of 3 meters. All of these unrealistic attributes is removed, before continuing with the data. The figures below show the distribution of the numerical variables in the two dataset.

![Character meta dataset before cleaning](figures/dist_and_clean/before_cleaning_character.png)

![Character meta dataset before cleaning](figures/dist_and_clean/before_cleaning_movie.png)

It is clear to see, that there are some extreme outliers in both datasets. Some are the variables also look very heavy-tailed and might need to be transformed.

After removing outliers, the distribution are as shown below.

![Character meta dataset before cleaning](figures/dist_and_clean/after_cleaning_character.png)

![Character meta dataset before cleaning](figures/dist_and_clean/after_cleaning_movie.png)


Looking at the box plot, we notice that **Movie box office revenue** has a very skewed distribution. The left histogram below shows, that very few movies have a very high revenue, and a lot of movie have a much lower revenue. Therefore we transform this variable to make it normal distributed, as shown on the right. <mark>er det relevant?</mark>

![Movie box office revenue before and after log transformation](figures/dist_and_clean/log_movie_box_revenue.png)

However, the value of the US dollar is not the same in 2023 as it was over a hundred years ago. The plot below shows the increase of revenue and value of the US dollar through the years Therefore we will have to <mark>tage højde for </mark> inflation.

![Inflation of the US dollar's effect on revenue](figures/dist_and_clean/inflation_plots.png)
