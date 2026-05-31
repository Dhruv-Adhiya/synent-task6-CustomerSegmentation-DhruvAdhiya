# Customer Segmentation using K-Means Clustering

## Problem Statement

Customer segmentation is the process of dividing customers into distinct groups based on their characteristics and behavior. Businesses use customer segmentation to better understand their customers, improve marketing strategies, and provide personalized services.

The objective of this project is to analyze customer data from a shopping mall and group customers into meaningful segments using the K-Means Clustering algorithm. These segments can help businesses identify different customer types and make data-driven decisions.

---

## Dataset Details

The project uses the **Mall Customer Dataset**, which contains demographic and spending information of mall customers.

### Features

| Column Name | Description |
|------------|-------------|
| CustomerID | Unique customer identifier |
| Gender | Customer gender |
| Age | Customer age |
| Annual Income (k$) | Annual income in thousand dollars |
| Spending Score (1-100) | Score assigned based on customer spending behavior |
| Education | Educational qualification of customer |
| Marital Status | Customer marital status |

### Dataset Characteristics

- Dataset Type: Structured Tabular Data
- Format: Excel (.xlsx)
- Number of Records: Varies according to dataset version
- Target: Unsupervised Learning (No target variable)

---

## Approach

### 1. Data Loading

- Loaded the Mall Customer dataset using Pandas.
- Inspected the dataset structure and column information.

### 2. Data Preprocessing

- Checked for missing values.
- Renamed columns for easier processing.
- Converted categorical features such as Gender, Education, and Marital Status into numerical values using Label Encoding.

### 3. Feature Selection

Selected the following features for clustering:

- Age
- Annual Income
- Spending Score
- Gender
- Education
- Marital Status

### 4. Feature Scaling

- Applied StandardScaler to standardize the features.
- Scaling ensures that all features contribute equally during clustering.

### 5. Optimal Cluster Selection

- Used the Elbow Method to determine the optimal number of clusters.
- Calculated WCSS (Within Cluster Sum of Squares) for cluster values ranging from 1 to 10.
- Identified the optimal cluster count based on the elbow point in the graph.

### 6. K-Means Clustering

- Applied the K-Means Clustering algorithm.
- Assigned each customer to a cluster.
- Added cluster labels to the original dataset.

### 7. Cluster Visualization

- Visualized customer segments using scatter plots.
- Displayed cluster centroids for better interpretation.

### 8. Cluster Evaluation

- Calculated the Silhouette Score to evaluate clustering quality.
- Analyzed average customer characteristics within each cluster.

---

## Results

### Generated Outputs

- Elbow Method Visualization (`elbow_method.png`)
- Customer Segmentation Plot (`customer_segments.png`)
- Segmented Dataset (`Mall_Customers_Segmented.xlsx`)

### Key Findings

The K-Means algorithm successfully grouped customers into distinct segments based on demographic and spending behavior.

Typical customer groups identified include:

- High Income – High Spending Customers
- High Income – Low Spending Customers
- Low Income – High Spending Customers
- Low Income – Low Spending Customers
- Average Income – Average Spending Customers

### Business Insights

- High-spending customers can be targeted with premium products and loyalty programs.
- Low-spending customers may benefit from promotional offers and discounts.
- High-income customers with low spending indicate potential opportunities for personalized marketing.
- Customer segmentation helps businesses improve customer retention and increase revenue through targeted strategies.

### Performance Metric

- Silhouette Score was used to measure clustering effectiveness.
- Higher silhouette scores indicate better separation between customer segments.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn

- 
