# Unsupervised Machine Learning

## Cryptocurrency Evaluator

This unsupervised learning model imports data on cryptocurrencies and identifies groupings based on several data points, or dimensions.

#### Import and Clean

Dependencies and the data are imported into python pandas. The crypto data is cleaned by dropping those currencies that are not publicly traded, those that have not been mined, and any with incomplete information. Also drops non-essential data to the model, which are the currency names.

#### Preprocessing

After importing and cleaning, the data is preprocessed by using pandas get dummies to convert categorical names into binary. The data is then scaled.

#### Dimension Reduction

Next, the dimensions are reduced using two methods. The first is PCA, or Principal Component Analysis. This linearly reduces dimensions, or inputs, from 98 to 74 but preserves 90% of the explained variance. The second is t-SNE, which reduces dimensions by grouping neighbors. It is mainly used to visualize data. In this case a scatter plot is constructed and shows some distinct clusters.

#### Cluster Analysis

The final step is to determine the number of clusters, or k, using K-Means cluster analysis. An elbow curve is constructed to determine the best k, meaning the lowest k possible with an acceptably low inertia, or distance to the central point (k).

#### Conclusion/Recommendation

This model first reduced the dimensions of the data using PCA and t-SNE. This allowed a visualization of the data. The scatter plot showed two main clusters with several other clusters surrounding. 

K-Means analysis resulted in an elbow chart which suggests a k (number of clusters) as either 3 or 4, and I decided 4 had a lower inertia.  

With those results, it seems the data can be clustered together and I recommend grouping the data into 4 clusters.