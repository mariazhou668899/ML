# HW2 Brief Report
### Part 1 : All Cuisines Types Clustering Visualization
  - The ingredients dataset has clear region boundary, from the same region cuisines have similar ingredients.
  - The Flavor dataset has no region boundary, as different cuisines share common flavors.

### Part 2 : PCA Analysis
  - For the original ingredients dataset (yummly_ingrX.pkl), the dataset originally contained 236 dimensions. After applying PCA, 208 components were retained, capturing 95% of the variance in the data. The percentage contribution of each component is detailed in the corresponding output section.
  - For the original flavor dataset (yum_tfidf.pkl), the dataset originally had 1108 dimensions. Following PCA, 98 components were retained, also capturing 95% of the variance. The percentage contribution of each component is similarly listed in the corresponding output section.
  - While both datasets achieve similar levels of variance retention, the ingredients dataset offers a more nuanced representation by preserving a greater number of components. This could potentially provide more detailed information for subsequent analyses, such as clustering or classification.

### Part 3 : K-Mean Clustering
  - Despite applying PCA (which captures 95% of the variance for both ingredients and flavor datasets) to reduce the dataset's dimensions, the K-Means algorithm struggles with high-dimensional data due to the "curse of dimensionality." This challenge can lead to suboptimal clustering results.
  - For both ingredients and flavor datasets, the elbow method and silhouette score fail to provide a clear choice for the optimal number of clusters (N). The elbow method shows a continuous downward trend without any clear flattening, and the silhouette score peaks at around 0.12 (N=2), a low value suggesting poor cluster separation. Additionally, the silhouette plot exhibits jagged fluctuations, further indicating the difficulty in defining distinct cluster boundaries.
  - The K-means model tends to perform better when the dataset includes regional character that allow for distinct separation between clusters.
  - The ingredients dataset can be distinguished by region cuisine, but still has some overlapping when using K-means model.
  - The flavor dataset is challenging to distinguish by region cuisine, as different cuisines share some common flavors.

 **1. K-Mean Clustering--- Ingredients**

  For this part, I did 2 experiments, one is for 4-cuisine-type, one is for all-cuisine-type

 **(1) For 4-Cuisine-Type**

    - K-means model can't use the elbow and silhouette score to detect the reasonable N in this 4-cuisine-types dataset, which maybe indicate this model is not applying this dataset quite well.
    - From the scatter plot, assigned N=4 (as we know the cuisine results from original data), the scatter plot partially proves the elbow and silhouette score conclusion.
    - There are lots of overlapping spots on the Italian and French. This reflects K-means model will cluster Italian and Frensh cuisines into the same group based on their ingredients, which is reasonable considering their similar cuisines.
    - For this dataset, the the K-means will dived them into 3 reasonable groups based on ingredients:
      - Italian and Frensh
      - Indian
      - Japanese

 **(2) For All-Cuisine-Type**

    - K-means model can't use the elbow and silhouette score to detect the reasonable N, which maybe indicate this model is not applying this all cuisines dataset.
    - From the scatter plot, assigned N=25 (as we know the cuisine results from original data) or other values, the scatter plot proves the elbow and silhouette score conclusion. There are lots of overlapping spots on the plot. It is very hard to observe distinguish clusters.
    - However, from the scatter plot, if we could find that the same continents cuisines coming from the close countries share more same ingredients because they have similar color.

 **2. K-Mean Clustering--- Flavor**

 **(1) For All-Cuisine-Type**

    - The K-means model can't effectively use the elbow and silhouette scores to determine a reasonable number of clusters (N). This suggests that the model may not be suitable for the entire dataset of cuisines.
    -  From the scatter plot, assigning N=21 (which aligns with known cuisine results from the original flavor data) or other values don't help to do clustering. The scatter plot shows that different colored dots are scattered throughout the plot, indicating a lack of clear clustering.
    - The flavor dataset is challenging to distinguish by cuisine, as different cuisines share some common flavors.

# Part 4 : DBSCAN, Hierarchical and GMM Clustering
- For the ingredients and flavor datasets, all these models (DBSCAN, Hierarchical and GMM Clustering) don't work well even though I use the PCA((which captures 95% of the variance for both ingredients and flavor datasets) ) to reduce dimensions and use optimizations for models. There are lots of overlapping. It is hard to find the clear boundary.
- The DBSCAN performance the worst no matter the ingredients dataset or flavor dataset.
- The Hierarchical and GMM Clustering performances a little bit well for the ingredient dataset, but still bad for the flavor dataset. Among these 2 models, the GMM is better than Hierarchical.

