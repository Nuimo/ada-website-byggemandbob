## Bag-of-words | Text Data Magic: From words to 26 cool clusters

We decide to cluster the movies based on similarity score between words in the plot summaries. To prepare the plot summaries for analysis, we apply stemming, lemmatization, and stopword removal to our text data. Next, we use TF-IDF for text representation. For dimensionality reduction, we aim for 95% variance retention, leading to component reduction. We then employ K-means clustering, determining the optimal k=30 based on the silhouette score and performance reasons, resulting in 30 clusters. After filtering out clusters with 100 samples or fewer, we end up with 26 clusters.

The clusters are formed by similarity between words in the movies' plot summaries. Therefore, each cluster contains a list of words ranked from most important to least important. A way to represent the cluster, and what words characterize them, is by the word clouds seen below. Each word in the word cloud is represented in the cluster, and the bigger the word, the more significant it is for that cluster. The plot below shows the word clouds for cluster five to eight.

![Example of word clouds for cluster 5, 6, 7 and 8](figures/nlp/word_cloud_example.png){:width="65%"}

We see that the four cluster seen here have some clear tendencies as well. Looking at cluster 6 the most significant (biggest) words seem to fall in the same category: alien, ship, kill and earth.

## Rating & revenue
But let us circle back to our goal of this analysis: to create a movie with **highest possible revenue** and **best possible rating**. Let's see how these plot summaries can help us with that!

Each cluster contains a number of movies, each with a given revenue and rating. To check if there is a significant difference between revenue and rating in the cluster, we randomly choose 100 movies from each cluster and calculate the mean revenue and rating. We do this 100 times and calculate the average of all the means from all the samples.

The average mean of each cluster for both rating and revenue is plotted below with error bars indicating the 95% confidence interval.

![Average rating and revenue for each cluster](figures/nlp/nlp_rev_rating_subplots.png){:width="100%"}


The plots reveal that the confidence intervals for several of the clusters do not overlap, indicating a statistically significant difference in both revenues and ratings among the clusters. In the plot above, the cluster have been arranged in increasing order of both rating and revenue. However, if we arrange the cluster only with increasing revenue, we see that the two attributes don't go hand in hand. Actually, one of the movie clusters with the highest revenue has the worst ratings (cluster 18).

![Average rating and revenue for each cluster](figures/nlp/nlp_rev_rating_both_plots.png){:width="80%"}

To get a more clear picture of what plot summaries yield a high rating and revenue, we have chosen the top 3 and bottom 3 movies for both rating and revenue. We then had ChatGPT-4 ([OpenAI](https://openai.com/)) create a movie poster for the top and bottom clusters based on their most significant words. This visualization helps us to understand what kind of movies get a high rating and revenue, and which movies fail to do so.

### Top-rated movies - The clusters that yield high quality 
Maybe not so surprising, we find that the top-rated movies look like classics most could put a real movie title to. At the very top we find all the war movies which interestingly seem mostly to include movies from World War II. 
A classic western is to be found in the second place and in third we see the crime-dramas that often relies on heavier and more complex plots.  

![Average rating and revenue for each cluster](figures/posters/best_rating_final.png){:width="100%"}

### Lowest rated movies - The clusters that reviewers slaughter
In this end of the scale we find the movies that did not do well with reviewers. The worst and third worst rated clusters looks respectively like the classic evil doctor/virus/epidemic turns into a monster and the alien invasion movies that we have all seen. These plots might be to far reached to fall into the likes of the typical reviewer. In the second to last place we find movies that seem as if they could be based on video-games. One common view of these movies are that they just do not live up to the expectations of the enthusiastic "gamers". 

![Average rating and revenue for each cluster](figures/posters/worst_rating_final.png){:width="100%"}

### Highest grossing movies - The clusters that bring back money
Again not very surprisingly we see here the posters that most of us probably could imagine hanging in front of the cinemas. These are what we can call the blockbusters. You might get the feeling that you have already seen these films from looking at the posters. 

Looking at the highest grossing cluster we recognize the typical action movie, involving some government, a range of armed men and lots of explosions. 

In second place we find our typical Sci-Fi films with some kind of threat to the human race, with lots of CGI and some very thin plot about saving the world. What is very interesting about this one is that is falls into both the top 3 highest grossing films and in the bottom 3, when looking at ratings. We could imagine this to be caused by an over-promising trailer with high budgets, but then not performing when it comes to the quality of the story. 
In third place it shows that apparently a classic drama surrounding a wedding draws a lot of viewers. 

![Average rating and revenue for each cluster](figures/posters/best_rev_final.png){:width="100%"}

### Lowest grossing movies - The clusters that make you poor
Here we find some og the more some of the softer plots. The storylines do not look as obvious as the best performing movies. Though we can still get the general gist from these posters. Interestingly we see a lot of women represented in the posters. The plots seem to revolve around families and more wholesome plot-lines than the action and "explosive" themes we saw in the top grossing movies.

![Average rating and revenue for each cluster](figures/posters/worst_rev_final.png){:width="100%"}


### Combined score - The golden standard 
By normalizing the rating and the revenue we have made a combined score to determine the clusters that perform best overall. 

![Average rating and revenue for each cluster](figures/nlp/gold_plot.png){:width="100%"}
From the graph we can see that the confidence interval seem to overlap alot. But following our performed ANOVA test we see that the clusters overall score are indeed significant!

![Average rating and revenue for each cluster](figures/posters/gold_final.png){:width="100%"}
From this we get these three films that we have already touched upon. Their clusters do, from our research, make the best combined performance when considering both their rating and their revenue. Not to bad huh?! 

