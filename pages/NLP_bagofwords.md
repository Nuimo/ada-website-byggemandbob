### Bag-of-words | Text Data Magic: From Words to 26 Cool Clusters

In our project, we started with preprocessing, applying stemming, lemmatization, and stopword removal to our text data. Next, we used TF-IDF for text representation. For dimensionality reduction, we aimed for 95% variance retention, leading to component reduction. We then employed K-means clustering, determining the optimal k=30 based on the silhouette score and performance reasons, resulting in 30 clusters. After filtering out clusters with less than 100 samples, we ended up with 26 clusters.


-------
- preprocessing, stemming, lemmatization, stopword removal, 
- We then proceeded to use a TF-IDF
- component reduction, dimensionality reduction, how many components you need, 95%.
- Kmeans, then proceeded find the optimal k, based on the silhouette score and CPU score, ended with k=30. 30 clusters
- (above 1 small block)
- sorted out the cluster with less than 100 samples, we then ended up with 26 clusters.

### Rating & Box Office
We concluded our analysis with the determination that the average rating was x (as illustrated in the provided image), and the revenue was also distinctly represented in another graph. Together, these two combined formed graph X.

Our analysis revealed that the confidence intervals for the clusters did not overlap, indicating a statistically significant difference in both revenues and ratings among the clusters.

Further, we focused on identifying the top three and bottom three clusters. For each of these six clusters, we created word clouds to visually represent the most frequent and significant terms associated with them. Additionally, we envisioned a 3x2 layout showcasing ChatGPT-generated movie posters, each corresponding to a specific cluster. This layout places each word cloud next to its related movie poster, providing creative and also quite fun textual and visual data representations.


-------
- We ended up with the rating being x (IMG)
- and the revenue being (IMG)
- together they form X.

- Confidence intervals don't overlap it is clear that the clusters have significantly different revenues and ratings.

- We then take a look at the three best, three worst, 
- wordclouds
- perhaps a 3x2 of the movie posters from chatGPT.
- wordcloud next to generate movie poster image.

- (maybe make a combination, which movie should you make to have a high revenue and rating)
