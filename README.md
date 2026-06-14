# Customer-Segmentation-Dashboard

# Customer Segmentation Using K-Means Clustering and Power BI

## 📌 Project Overview

This project focuses on customer segmentation using Machine Learning and Business Intelligence techniques. The objective is to identify distinct customer groups based on purchasing behavior and business metrics, enabling organizations to make data-driven marketing and customer retention decisions.

The project combines **Python**, **K-Means Clustering**, and **Power BI** to analyze customer data, generate meaningful customer segments, and visualize insights through an interactive dashboard.

---

## 🎯 Objectives

* Analyze customer purchasing behavior.
* Segment customers into meaningful groups using K-Means Clustering.
* Identify high-value and low-value customers.
* Visualize customer segments and business insights using Power BI.
* Provide actionable recommendations for targeted marketing strategies.

---

## 🛠️ Technologies Used

### Programming & Analytics

* Python
* Pandas
* NumPy
* Scikit-Learn
* Matplotlib
* Seaborn

### Business Intelligence

* Power BI
* DAX

### Dataset

* Excel (.xlsx)
* CSV (.csv)

---

## 📂 Dataset Description

The dataset contains sales transaction records with the following attributes:

| Column   | Description        |
| -------- | ------------------ |
| order_id | Unique Order ID    |
| customer | Customer Name/ID   |
| product  | Product Name       |
| category | Product Category   |
| region   | Sales Region       |
| quantity | Quantity Purchased |
| revenue  | Revenue Generated  |
| profit   | Profit Earned      |
| year     | Order Year         |
| month    | Order Month        |

---

## 🔍 Data Preprocessing

The following preprocessing steps were performed:

1. Removed unnecessary fields.
2. Converted data types where required.
3. Aggregated transaction-level data into customer-level metrics.
4. Generated customer KPIs:

   * Total Revenue
   * Total Profit
   * Total Quantity
   * Total Orders
5. Standardized features using StandardScaler.

---

## 🤖 Machine Learning Approach

### K-Means Clustering

K-Means clustering was applied to group customers based on:

* Total Revenue
* Total Profit
* Total Quantity
* Total Orders

### Feature Scaling

Standardization was performed before clustering:

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)
```

### Elbow Method

The optimal number of clusters was determined using the Elbow Method.

```python
from sklearn.cluster import KMeans

wcss = []

for i in range(1,11):
    model = KMeans(
        n_clusters=i,
        random_state=42,
        n_init=10
    )
    model.fit(X_scaled)
    wcss.append(model.inertia_)
```

The Elbow Method suggested:

**Optimal Clusters (K) = 4**

---

## 📊 Customer Segments

After clustering, customers were categorized into four business-friendly groups:

| Segment              | Description                                       |
| -------------------- | ------------------------------------------------- |
| VIP Customers        | Highest revenue and profit contribution           |
| High Value Customers | Strong purchasing behavior and high profitability |
| Regular Customers    | Moderate revenue and consistent purchases         |
| Low Value Customers  | Lowest spending and profitability                 |

---

## 📈 Cluster Visualization

Customer segments were visualized using a scatter plot based on:

* Total Revenue
* Total Profit

This visualization clearly demonstrates the separation of customer groups and the effectiveness of the clustering algorithm.

---

## 📉 Power BI Dashboard

### Dashboard Features

#### KPI Cards

* Total Customers
* Total Orders
* Total Revenue
* Total Profit

#### Customer Distribution

* Segment-wise customer count

#### Revenue Analysis

* Revenue by Customer Segment

#### Profit Analysis

* Profit by Customer Segment

#### Customer Performance

* Scatter Plot Analysis

#### Customer Contribution

* Top Customers by Revenue

---

## 📋 Key Insights

### VIP Customers

* Generate the highest revenue and profit.
* Require retention-focused strategies.
* Ideal candidates for loyalty programs and premium offers.

### High Value Customers

* Significant contributors to business growth.
* Suitable for upselling and cross-selling opportunities.

### Regular Customers

* Consistent purchasers with moderate value.
* Can be nurtured through engagement campaigns.

### Low Value Customers

* Lowest revenue contribution.
* May benefit from promotional campaigns and discounts.

---

## 🚀 Business Recommendations

### VIP Customers

* Exclusive rewards programs
* Personalized marketing
* Premium support services

### High Value Customers

* Cross-selling opportunities
* Product recommendations
* Membership upgrades

### Regular Customers

* Customer engagement campaigns
* Seasonal offers
* Loyalty incentives

### Low Value Customers

* Discount campaigns
* Reactivation programs
* Personalized promotions

---

## 📊 Project Workflow

```text
Sales Dataset
      │
      ▼
Data Cleaning
      │
      ▼
Customer Aggregation
      │
      ▼
Feature Scaling
      │
      ▼
K-Means Clustering
      │
      ▼
Customer Segments
      │
      ▼
Export CSV
      │
      ▼
Power BI Dashboard
      │
      ▼
Business Insights
```

---

## 📁 Project Structure

```text
Customer-Segmentation-Project
│
├── data
│   ├── Sales_sample_data.xlsx
│   └── customer_segments_final.csv
│
├── notebooks
│   └── Customer_Segmentation.ipynb
│
├── dashboard
│   └── Customer_Segmentation.pbix
│
├── screenshots
│   ├── elbow_method.png
│   ├── kmeans_clusters.png
│   └── dashboard.png
│
└── README.md
```

---

## 📌 Results

* Successfully segmented customers into four meaningful groups.
* Identified customer behavior patterns and revenue contribution.
* Built an interactive Power BI dashboard for business stakeholders.
* Demonstrated the integration of Machine Learning and Business Intelligence techniques.

---

## 👨‍💻 Author

**JK**
AI & Data Science Student

### Skills Demonstrated

* Data Cleaning
* Exploratory Data Analysis
* Machine Learning
* K-Means Clustering
* Customer Analytics
* Data Visualization
* Power BI
* Business Intelligence
* Python Programming
