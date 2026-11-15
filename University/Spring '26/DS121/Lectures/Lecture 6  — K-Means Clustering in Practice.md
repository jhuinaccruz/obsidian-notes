__Clustering Workflow__:
1. Prepare data by cleaning, normalizing it and selecting its features
	- Use MDS or similar to see if clusters exist
2. Choose `k` (how many clusters?)
3. Run the algorithm that fits `k`-means to the data
4. Interpret the data to understand what each cluster represents
5. Validate the data and decide if the clusters are meaningful

__Heatmaps__: Show raw values/distances,
- Hard to interpret

__Multidimensional Scaling__: Finds 2D coordinates where distances match the original high-dimensional distances
1. Start with random 2D positions
2. Compare distances in 2D to true distances in more dimensions
3. Adjust positions to reduce mismatch
4. Repeat until distances are as close as possible

__Examining Clusters__:
- For synthetic data, compare using its "real" labels
- For real data, examine the clusters to understand them

__Inertia__: The cost of choosing a certain `k`
- Has an inverse relationship with `k`

>[!abstract] Clustering Workflow
 >1. Visualize data with MDS or similar to see if clusters exist
 >2. Cluster by running `k`-means with the chosen `k`
 >3. Validate by checking the distance matrix, comparing to ground truth if available
 >4. Interpret by examining centroid and cluster members
 >5. Iterate with different `k` values and comparing results
 