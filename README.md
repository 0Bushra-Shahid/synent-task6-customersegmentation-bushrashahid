# Customer Segmentation using K-Means Clustering

## Problem Statement
Malls and retail businesses often have diverse customers with different spending habits and income levels. Without grouping customers, it becomes difficult to design targeted marketing strategies. This project aims to segment mall customers into distinct groups based on their **Annual Income** and **Spending Score**, so that marketing efforts can be tailored to each group's behavior.

## Dataset Details
- **Dataset Name:** Mall Customer Dataset
- **Source:** Kaggle
- **Records:** 200 customers
- **Features:**
  - CustomerID
  - Gender
  - Age
  - Annual Income (k$)
  - Spending Score (1-100)

## Approach
1. **Data Loading & Exploration** – Loaded the dataset and checked for missing values, data types, and summary statistics.
2. **Feature Selection** – Selected `Annual Income (k$)` and `Spending Score (1-100)` as the two key features for clustering.
3. **Elbow Method** – Used the Within-Cluster-Sum-of-Squares (WCSS) method to determine the optimal number of clusters, which was found to be **5**.
4. **K-Means Clustering** – Applied K-Means clustering with `k=5` to group customers based on their behavior.
5. **Visualization** – Plotted the clusters using a scatter plot with cluster centroids to visually confirm the segmentation.
6. **Insight Generation** – Calculated average Age, Income, and Spending Score per cluster to interpret and label each customer segment.

## Results

Using K-Means clustering, mall customers were segmented into **5 groups**:

| Cluster | Avg Age | Avg Income (k$) | Avg Spending Score | Segment Label |
|---|---|---|---|---|
| 0 | 43 | 55 | 50 | Average Customers |
| 1 | 33 | 87 | 82 | Premium/Target Customers |
| 2 | 25 | 26 | 79 | Careless Spenders |
| 3 | 41 | 88 | 17 | Cautious Customers |
| 4 | 45 | 26 | 21 | Budget-Conscious Customers |

### Key Insights
- **Cluster 1 (Premium/Target Customers)** is the most valuable segment — high income and high spending. Marketing efforts should prioritize this group.
- **Cluster 3 (Cautious Customers)** has high income but low spending, representing an opportunity to increase engagement through personalized offers.
- **Cluster 2 (Careless Spenders)** are young customers with low income but high spending — a potential target for loyalty or credit-based offers.
- **Cluster 4 (Budget-Conscious Customers)** have both low income and low spending, requiring value-focused promotions.
- **Cluster 0 (Average Customers)** represents the general customer base with balanced income and spending.

These insights can help the mall design targeted marketing strategies for each customer segment.

## Tools & Libraries Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn (KMeans)

## How to Run
1. Clone this repository
2. Install required libraries: `pip install pandas numpy matplotlib seaborn scikit-learn`
3. Open `segmentation.ipynb` in Jupyter Notebook
4. Run all cells in order

## Author Name
  Bushra Shahid
  
