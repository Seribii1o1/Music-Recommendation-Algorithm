# Music Recommendation Algorithm (Unsupervised)

<u>Background</u>

I analyzed a dataset of songs(1950 to 2011), their lyrical features, and their lyrical content in order to discover clusters which will then be used to recommend music for a hypothetical user.

This dataset contains a mix of lyrical and continuous variables pulled from a 2020 research paper titled [Music Dataset: Lyrics and Metadata from 1950 to 2019](https://data.mendeley.com/datasets/3t9vbwxgr5/3).

I created a comprehensive machine learning pipeline that satisfies the patterned steps of a classic machine learning project. 

<u>Project Content</u>

1. Hypothesis formulation with initial EDA: notebook with univariate, bivariate, multivariate exploratory analysis, and relevant graphs

2. Data cleaning, pre-processing, and dimensionality reduction: notebook for cleaning and wrangling dataset. Might include dropping null values, removing unnecessary columns, removing outliers, and potentially fixing incorrectly formatted data. Dropped columns that had strong correlation and linearity.

(note: for now it would be best to drop the “lyrics” column).
I saved this dataframe as a new csv file to be used in the next step.

3. Model creation, hyperparameter search, and model evaluation
Once you have cleaned and reduced this dataset, we will then create a notebook where we will implement a KMeans Clustering or any other clustering algorithm of your choice on your training dataset.
After initial training, evaluate the best number of clusters using one of the cluster identification techniques.
After generating the clusters for each sample in the training dataset, save these cluster-labels as a new column in your dataframe and save this dataframe for further analysis.

4. New Sample Prediction

Finally, I applied the trained machine learning algorithm on the following test dataset, in order to generate cluster labels for each new sample.
After generating these clusters, I saved these labels as a new column in the test dataset and save this subsequent dataframe for further analysis.

5. Report

To conclude this project, I answered the following 5 questions in the report file:

1. Which insights did you gain from your EDA? Were any columns highly correlated? If so, name them.

2. How did you determine which columns to drop or keep? If your EDA informed this process, explain which insights you used to determine which columns were not needed. 

3. What was the optimal number of clusters in your cluster model? Explain how you determined this value.

4. Take a look at the respective songs that fell into your clusters. Describe these clusters in human terms to the best of your ability using the columns in your dataset (for example high-gospel songs, low-gospel songs, etc). Feel free to listen to these songs as well to get a sense of what nuance your algorithm picked up on.

5. Take a look at the clusters that your algorithm assigned to your test samples. Based on these clusters, which songs would you recommend to this user?

6. Lyrical Sentiment Analysis

I created an additional notebook that contains a Word2Vec model to analyze the lyrical content of our “lyrics” column. 
After training a Word2Vec model, I got a list of vectors of the words used in this dataset, and reduce these vectors down to two components using PCA analysis.
I visualized lyrics and their PCA components using a scatter-plot to note the lyrical content of the dataset.



