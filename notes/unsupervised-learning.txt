Unsupervised Machine Learning

is a type of machine learning where the model works without labelled data. It learns patterns on its own by grouping similar data points or finding
hidden structures without any human intervention.
- it is used for tasks like clustering, dimensionality reduction and Association Rule learning.
- Helps identify hidden patterns in data
- Useful for grouping, compression and anomaly detection.

Working of Unsupervised Learning:

1. Collect unlabeled data
- gather a dataset without predefined labels or catergories
2. Select an Algorithm
- Choose a suitable unsupervised algorithm such as clustering like K-Means, association rule learning like Apriori or dimensionality reduction like PCA based on the goal.
3. Train the Model on Raw Data
- Feed the dataset to the algorithm
- algorithm looks for similarities, relationships or hidden structures within the data
4. Group or Transform Data
- The algorithm organizes data into groups (clusters), rules or lower-dimensional forms without human input.
5. Interpret and Use Results
- Analyze the discovered groups, rules or features to gain insights or use them for further task like visualization, anomaly detection or as input for other models.

Unsupervised Learning Algorithms: There are mainly 3 types of Unsupervised Algorithms that are used

1. Clustering Algorithms: Clustering is an unsupervised learning technique that groups unlabeled data into clusters based on similarity. Its goal is to discover
patterns or relationships within the data without any prior knowledge or categories or labels.
- Groups data points that share similar features or characteristics
- Helps find natural groupings in raw; unclassified data.
- Commonly used for customer segmentation, anomaly detection and data organization.
- Works purely from the input data without any output labels.
- Enables understanding of data structure for further analysis or decision-making.

Some common clustering algorithms:

- K-means Clustering https://www.geeksforgeeks.org/machine-learning/k-means-clustering-introduction/ : Groups data into K clusters based on how close the points
are to each other.
- Hierarchical Clustering https://www.geeksforgeeks.org/machine-learning/hierarchical-clustering/ : Creates clusters by building a tree step-by-step, either merging or splitting groups
- Density-Based Clustering (DBSCAN) https://www.geeksforgeeks.org/machine-learning/dbscan-clustering-in-ml-density-based-clustering/: Finds clusters in dense areas
and treats scattered points as noise.
- Mean-Shift Clustering https://www.geeksforgeeks.org/machine-learning/ml-mean-shift-clustering/ : Discovers clusters by moving points toward the most crowded areas.
- Spectral Clustering https://www.geeksforgeeks.org/machine-learning/spectral-clustering/ : Groups data by analyzing connections between points using graphs

2. Association Rule Learning :

Association rule learning https://www.geeksforgeeks.org/machine-learning/association-rule/ is a rule-based unsupervised learning technique used to discover interesting
relationships between variables in large datasets. It identifies patterns in the form of "if-then" rules, showing how the presence of some items in the data implies the presence of others.
- Finds frequent item combinations and the rules connecting them.
- Commonly used in market basket analysis to understand product purchase relationships.
- Helps retailers design promotions and cross-selling strategies

Some common Association Rule learning algorithms:
- Apriori Algorithm https://www.geeksforgeeks.org/machine-learning/apriori-algorithm/: Finds patterns by exploring frequent item combinations step-by-step.
- FP-Growth Algorithm https://www.geeksforgeeks.org/machine-learning/frequent-pattern-growth-algorithm/: An Efficient Alternative to Apriori. It quickly identifies
frequent patterns without generating candidate sets.
- Eclat Algorithm https://www.geeksforgeeks.org/machine-learning/ml-eclat-algorithm/: Uses intersections of itemsets to efficiently find frequent patterns
- Efficient Tree-based Algorithms https://www.geeksforgeeks.org/dsa/introduction-to-tree-data-structure/: Scales to handle large datasets by organizing data in tree
structures

3. Dimensionality Reduction https://www.geeksforgeeks.org/machine-learning/dimensionality-reduction/ :

the process of decreasing the number of features or variables in a dataset while retaining as much of the original information as possible. This technique helps simplify complex
data making it easier to analyze and visualize. It also improves the efficiency and performance of machine learning algorithms by reducing noise and computational cost.
- It reduces the dataset's feature space from many dimensions to fewer, more meaningful ones.
- Helps focus on the most important traits or patterns in the data.
- Commonly used to improve model speed and reduce overfitting.

Some popular Dimensionality Reduction algorithms:
- Prinicpal Component Analysis(PCA) https://www.geeksforgeeks.org/data-analysis/principal-component-analysis-pca/:
 Reduces dimenstions by transforming data into uncorrelated principal components
 - Non-negative Matrix Factorization (NMF) https://www.geeksforgeeks.org/machine-learning/non-negative-matrix-factorization/: Breaks data into non-negative parts to simplify representation.
 - Locally Linear Embedding (LLE) https://www.geeksforgeeks.org/machine-learning/locally-linear-embedding-in-machine-learning/: Reduces dimensions while preserving the relationships
 between nearby points.
 - Isomap https://www.geeksforgeeks.org/machine-learning/isomap-a-non-linear-dimensionality-reduction-technique/: Captures global data structure by preserving distances along a manifold


 Applications

 -Customer Segmentation: Algorithms cluster customers based on purchasing behavior or demographics, enabling targeted marketing strategies.
 -Anomaly Detection: Identifies unusual patterns in data, aiding fraud detection, cybersecurity and equipment failure prevention.
 - Recommendation Systems: Suggests products, movies or music by analyzing user behavior or preferences.
 - Image and Text Clustering: Groups similar images or documents for tasks like organization and content reccomendation.
 - Social Network Analysis: Detects communities or trends in user interations on social media platforms.

 Advantages

- Works with raw, unlabeled data, saving time and effort required for data annotation
- Finds hidden patterns and natural groupings in data that may not be easily identified by humans
- Handles large and complex datasets efficiently, including high-dimensional data.
- Helps detect anomalies and unusual data points without needing prior examples.

Challenges

- Noisy data and outliers can distort patterns and reduce the effectiveness of the model.
- Models may capture noise instead of menainful patterns, leading to overfitting.
- Lack of labeled data makes it difficult to guid the algorithm toward specific outcomes
- Results such as clusters may be difficult to interpret or many not clearly match real-world catergories