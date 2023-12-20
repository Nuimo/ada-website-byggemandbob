## How does gender representation influence movie revenue?

Let first take a look at the representation of male and female actors in movies over time.

![Male and female actor count on for each movie release year](figures/gender/gender_count_release_year.png){:width="50%"}

There is a trend over all years, that there are more male actors than female actors in movies. But has there been no change in the last century? Let us dive into that.

![Development of percentage of female actors over time](figures/gender/female_percentage_release_year.png){:width="50%"}

With a p-value of 0.10 of the linear regression, there has been no significant change of female characters in the past century. But looking at the plot, there seems to be a trend from 1980 and forward. Let us look at that.

![Development of percentage of female actors over time](figures/gender/female_percentage_release_year_filtered.png){:width="50%"}

With a p-value of 0.00 of the linear regression bt, there is has been a significant increase in female actors in the past century. But does gender even effect the box office revenue of the movie?

![Movie box office revenue given as a function of percentage of female actor in a given movie](figures/gender/female_percentage_revenue.png){:width="50%"}

With a p-value of 0.00, the linear regression above shows, that there is a significant decrease in the box office revenue for a movie, if there are more female actors. But is it really because people do not want to see females on screen, or could there be another explanation?

### Difference between male and female actors

We divide the character dataset into male and female character dataset. Looking at the attribute, the only relevant one to explore is **Actor age at movie release**.

![Male and female distribution](figures/gender/gender_age.png){:width="50%"}

The plot shows us, that there is a significant difference in the age of male and female actors. It indicates, that female actors generally are younger than male actors in movies.