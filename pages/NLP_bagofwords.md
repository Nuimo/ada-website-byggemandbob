## Bag-of-words | Text Data Magic: From Words to 26 Cool Clusters

We decide to cluster the movies based on similarity score between words in the plot summaries. To prepare the plot summaries for analysis, we apply stemming, lemmatization, and stopword removal to our text data. Next, we use TF-IDF for text representation. For dimensionality reduction, we aim for 95% variance retention, leading to component reduction. We then employ K-means clustering, determining the optimal $k=30$ based on the silhouette score and performance reasons, resulting in 30 clusters. After filtering our clusters with a 100 samples or less, we end up with 26 clusters.

The clusters are formed by similarity between words in the movies' plot summaries. Therefore, each cluster contains a list of words ranked from most important to least important. A way to represent the cluster, and what words characterize them, is by the word clouds seen below. Each word in the word cloud is represented in the cluster, and the bigger the word, the more significant it is for that cluster. The plot below shows the word clouds for cluster five to eight.

![Example of word clouds for cluster 5, 6, 7 and 8](figures/nlp/word_cloud_example.png){:width="65%"}

We see that the four cluster seen here have some clear tendencies as well. Looking at cluster 6 the most significant (biggest) words seem to fall in the same category: alien, ship, kill and earth.

## Rating & Revenue
But let us circle back to our goal of this analysis: to create a movie with **highest possible revenue** and **best possible rating**. Let's see how these plot summaries can help us with that!

Each cluster contains a number of movie, each with a given revenue and rating. To check if there is a significance difference between revenue and rating in the cluster, we take a randomly choose 100 movies from each cluster and calculate the mean revenue and rating. We do this 100 times and calculate the average of all the means from all the sample.

The average mean of each cluster for both rating revenue is plotted below with error bars indicating the 95% confidence interval.

![Average rating and revenue for each cluster](figures/nlp/nlp_rev_rating_subplots.png){:width="65%"}


The plots reveal that the confidence intervals for several of the clusters do not overlap, indicating a statistically significant difference in both revenues and ratings among the clusters. In the plot above, the cluster have been arranged in increasing order of both rating and revenue. However, if we arrange the cluster only with increasing revenue, we see that the two attributes don't go hand in hand. Actually, one of the movies with highest revenue has the worst ratings (cluster 18).

![Average rating and revenue for each cluster](figures/nlp/nlp_rev_rating_both_plots.png){:width="65%"}

To get a more clear picture of what plot summaries yield a high rating and revenue, we have chosen the top 3 and bottom 3 movies for both rating and revenue. We then had ChatGPT-4 <mark>reference</mark> create a movie poster for the top and bottom clusters based on their most significant words. This visualization helps us to understand what kind of movies get a high rating and revenue, and which movies fail to do so.

### Top Rated Movies - The clusters that yields high quality 
Maybe not very surprisingly we see here the posters that most of us probably could imagine hanging in front of the cinemas. These are what we can call the blockbusters. You might get the feeling that you have already seen these films from looking at the posters. 
Looking at the highest grossing cluster we recognise the typical action movie, involving some goverment, a range og armed men and lots og explotions. 
In second place we find our typical sifi films with so kind of threat to the human race, with lots of CGI and some very thin plot about saving the world.   
In third place it shows that apparently a classic drama surrounding a wedding draws a lot of viewers. 
![Average rating and revenue for each cluster](figures/posters/best_rating_final.png){:width="100%"}

### Lowest Rated Movies - The clusters that reviewers slaughter

![Average rating and revenue for each cluster](figures/posters/worst_rating_final.png){:width="100%"}

### Highest Grossing Miovies - The clusters that brings back money  

![Average rating and revenue for each cluster](figures/posters/best_rev_final.png){:width="100%"}

### Lowest Grossing Movies - The clusters that makes you poor

![Average rating and revenue for each cluster](figures/posters/worst_rev_final.png){:width="100%"}

