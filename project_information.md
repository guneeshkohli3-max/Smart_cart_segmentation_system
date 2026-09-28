# 🛒 SmartCart Segmentation System

An **Unsupervised Machine Learning** project that segments customers into meaningful groups based on their purchasing behavior, spending patterns, and demographic characteristics.

The goal of this project is to help businesses understand their customers better and design **targeted marketing strategies, personalized offers, and customer-specific campaigns**.

---

## 📌 Project Overview

SmartCart Segmentation System uses **customer segmentation techniques** to discover hidden patterns in customer data without using predefined labels.

Instead of manually defining customer groups, the system applies **clustering algorithms** to automatically identify customers with similar characteristics.

### Key Objectives

* Identify different customer segments.
* Analyze customer purchasing behavior.
* Discover high-value and low-value customer groups.
* Understand spending patterns across product categories.
* Support personalized marketing strategies.
* Visualize customer clusters for better interpretation.

---

## 🧠 Machine Learning Approach

This project follows an **Unsupervised Learning** approach.

### Algorithm Used

**K-Means Clustering**

K-Means groups customers into `K` clusters by minimizing the distance between customers and their respective cluster centroids.

### Basic Workflow

```text
Raw Customer Data
       ↓
Data Cleaning
       ↓
Exploratory Data Analysis
       ↓
Feature Selection
       ↓
Feature Encoding
       ↓
Feature Scaling
       ↓
Finding Optimal K
       ↓
K-Means Clustering
       ↓
Customer Segmentation
       ↓
Cluster Analysis & Visualization
```

---

## 📊 Dataset

The dataset contains customer-level information such as:

* Customer demographics
* Income
* Marital status
* Number of children
* Number of teenagers
* Customer enrollment information
* Recency
* Spending on different product categories
* Number of purchases through different channels

These features are used to identify similarities and differences between customers.

---

## 🔧 Technologies Used

* **Python**
* **Pandas** – Data manipulation
* **NumPy** – Numerical computation
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Scikit-learn** – Machine Learning
* **Jupyter Notebook**

---

## 🧹 Data Preprocessing

Before applying clustering, the dataset was cleaned and prepared.

### Steps performed

1. Removed irrelevant columns.
2. Handled missing values.
3. Identified and handled duplicate records.
4. Treated inconsistent categorical values.
5. Performed feature engineering.
6. Encoded categorical variables using **One-Hot Encoding**.
7. Scaled numerical features using feature scaling.
8. Prepared the final dataset for clustering.

---

## 🔍 Exploratory Data Analysis

EDA was performed to understand:

* Customer income distribution
* Spending behavior
* Purchase frequency
* Product category preferences
* Relationship between income and spending
* Customer demographics
* Outliers and unusual customer behavior

Visualizations were created using **Matplotlib and Seaborn**.

---

## 📐 Choosing the Number of Clusters

The optimal number of clusters was investigated using techniques such as:

### Elbow Method

The Elbow Method analyzes the **Within-Cluster Sum of Squares (WCSS)** for different values of `K`.

The value of `K` where the reduction in WCSS begins to slow down helps identify a suitable number of clusters.

### Silhouette Score

The **Silhouette Score** was also used to evaluate how well-separated the resulting clusters were.

A higher silhouette score generally indicates better-defined clusters.

---

## 🤖 K-Means Clustering

After determining an appropriate number of clusters, the K-Means algorithm was applied.

Conceptually:

```python
from sklearn.cluster import KMeans

kmeans = KMeans(
    n_clusters=K,
    random_state=42,
    n_init=10
)

clusters = kmeans.fit_predict(X_scaled)
```

The resulting cluster labels were then added to the customer dataset for further analysis.

---

## 📈 Customer Segmentation

The clustering process identifies groups of customers with similar behavioral characteristics.

For example, the resulting segments can be interpreted based on their:

* Spending levels
* Income
* Purchase frequency
* Product preferences
* Online/offline purchasing behavior
* Recency of purchases

The exact characteristics of each segment are determined by analyzing the cluster-level statistics.

---

## 💡 Business Insights

Customer segmentation can help businesses:

### 🎯 Targeted Marketing

Different customer groups can receive different marketing campaigns instead of sending the same campaign to everyone.

### 🛍️ Personalized Recommendations

Products and offers can be customized according to customer purchasing behavior.

### 💰 Identify High-Value Customers

Businesses can identify customers with high spending and strong purchasing activity.

### 🔄 Customer Retention

Customers showing reduced purchasing activity can be identified and targeted with retention campaigns.

### 📢 Campaign Optimization

Marketing budgets can be allocated according to the characteristics and potential value of different customer segments.

---

## 📊 Visualization

The customer clusters were visualized using dimensionality-reduction and plotting techniques to make the high-dimensional customer data easier to interpret.

Example:

```text
                Customer Segments

        ● ● ●
      ● ● ● ●              ▲ ▲ ▲
       ● ●                 ▲ ▲ ▲
                            ▲ ▲
              ■ ■ ■
            ■ ■ ■ ■
              ■ ■

        Cluster 1     Cluster 2     Cluster 3
```

Each cluster represents customers with similar characteristics.

---

## 🧪 Project Structure

```text
SmartCart-Segmentation-System/
│
├── data/
│   └── customer_data.csv
│
├── notebooks/
│   └── SmartCart_Segmentation.ipynb
│
├── README.md
│
└── requirements.txt
```

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the project

```bash
cd SmartCart-Segmentation-System
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Jupyter Notebook

```bash
jupyter notebook
```

Open the project notebook and run the cells sequentially.

---

## 📚 Concepts Demonstrated

This project demonstrates practical knowledge of:

* Unsupervised Machine Learning
* K-Means Clustering
* Customer Segmentation
* Exploratory Data Analysis
* Feature Engineering
* One-Hot Encoding
* Feature Scaling
* Elbow Method
* Silhouette Score
* Outlier Analysis
* Data Visualization
* Business-oriented ML interpretation

---

## 🔮 Future Improvements

Possible improvements include:

* Comparing K-Means with **DBSCAN** and **Hierarchical Clustering**
* Using **PCA** for dimensionality reduction
* Developing an interactive customer segmentation dashboard
* Adding automated customer recommendations
* Creating real-time customer segmentation
* Comparing multiple clustering evaluation metrics

---

## 👨‍💻 Author

**Guneesh Kohli**

B.Tech Computer Science & Engineering
New Horizon College of Engineering, Bengaluru

---

⭐ If you found this project useful, consider giving the repository a star!
