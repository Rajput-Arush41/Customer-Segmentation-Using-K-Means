# Mall Customer Segmentation using K-Means

An unsupervised machine learning project that groups 200 mall customers into
distinct segments based on their age, annual income and spending behaviour, so
that marketing and promotions can be targeted more effectively.

## Dataset
Mall Customers dataset (Kaggle): 200 records with Age, Annual Income (k$) and
Spending Score (1-100). The three continuous features were used for clustering.
There were no missing values or duplicates.

## Method
1. Standardized the features with `StandardScaler` so no single feature dominates the distance calculation.
2. Evaluated K = 1 to 10 with the elbow method (inertia) and K = 2 to 10 with silhouette scores.
3. Fitted the final `KMeans` model with K = 5 and a fixed `random_state` for reproducibility.
4. Converted the centroids back to original units to interpret each segment.

## Results
| Cluster | Segment | Avg Age | Avg Income (k$) | Avg Spending |
|---|---|---|---|---|
| 0 | Budget Buyers | 46 | 27 | 18 |
| 1 | Active Youth | 25 | 41 | 62 |
| 2 | Luxury Shoppers | 33 | 86 | 82 |
| 3 | Affluent Savers | 40 | 86 | 19 |
| 4 | Steady Consumers | 56 | 54 | 49 |

## Tech Stack
Python, pandas, NumPy, scikit-learn, matplotlib

## Files
- `ArushChhalaria_KMeans.ipynb`: full analysis notebook
- `ArushChhalaria_Report.pdf`: written report (if you upload it)
