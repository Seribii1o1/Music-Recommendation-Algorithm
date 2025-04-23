1. Which insights did you gain from your EDA? Were any columns highly correlated? If so, name them.

![Multivariate](/Users/sa26/Documents/GitHub/Music-Recommendation-Algorithm/docs/image-5.png)

Release date average is 1990, median is 1991, with most songs in 1975-2007 range. Average song is 73 words, median is 63, with most songs in between 42-93 words. Pop genre is the most popular, with hip hop as the least frequent. Sadness, violence, and word/life are the top three topics, with feelings as the lowest. 

Age and release_date are highly correlated. There is also a high correlation between hip hop genre and obscene topics.

2. How did you determine which columns to drop or keep? If your EDA informed this process, explain which insights you used to determine which columns were not needed. 

![Correlation](/Users/sa26/Documents/GitHub/Music-Recommendation-Algorithm/docs/image-4.png)

I added distinct genre columns and dropped the following six columns:
-Dropped Unnamed:0 (not in original list of variables)
-Based on the first heatmap in the EDA, I removed 'release_date' to reduce multicollinearity
-Removed lyrics for later analysis
-Dropped track_name and artist_name due to high amount of unique values
-Based on scaling and more heatmaps, I removed 'topic' to reduce multicollinearity 

3. What was the optimal number of clusters in your cluster model? Explain how you determined this value.

![Silhouette](/Users/sa26/Documents/GitHub/Music-Recommendation-Algorithm/docs/image-1.png)

The optimal number was 6 according to the elbow and silhouette methods. That is where the elbow "stopped" and the highest silhouette score.

4. Take a look at the respective songs that fell into your clusters. Describe these clusters in human terms to the best of your ability using the columns in your dataset (for example high-gospel songs, low-gospel songs, etc). Feel free to listen to these songs as well to get a sense of what nuance your algorithm picked up on.

![Model](/Users/sa26/Documents/GitHub/Music-Recommendation-Algorithm/docs/image-3.png)

C2 is the largest.
C0: low pop, very low country, very high blues
C1: low pop, low country, low blues
C2: very high pop, high country, high blues
C3: low pop, low country, very low blues
C4: low pop, low country, low blues
C5: very low pop, very high country, high blues

5. Take a look at the clusters that your algorithm assigned to your test samples. Based on these clusters, which songs would you recommend to this user?

![Test Model](/Users/sa26/Documents/GitHub/Music-Recommendation-Algorithm/docs/image-2.png)

I would recommend cluster one songs the most since most of the songs from the test sample fall into this cluster.