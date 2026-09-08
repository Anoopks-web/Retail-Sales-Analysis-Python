# 🛍️ Retail Sales Analysis Using Python

## 📌 Project Overview

This project performs **Retail Sales Data Analysis using Python and Pandas**.

The goal is to analyze customer behavior, product categories, sales performance, transaction patterns, and revenue using data analysis and visualization techniques.

---

## 📊 Dataset

The dataset contains retail transaction information with the following columns:

* Transaction ID
* Date
* Customer ID
* Gender
* Age
* Product Category
* Quantity
* Price per Unit
* Total Amount

---

## 🛠️ Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Google Colab
* GitHub

---

## 🔍 Data Analysis Process

### 1. Import Dataset

```python
import pandas as pd

df = pd.read_csv("retail_sales_dataset.csv")
df
```

### 2. Understand the Dataset

```python
df.shape
df.head()
df.tail()
df.info()
df.describe()
```

### 3. Check Data Quality

```python
df.isnull().sum()
df.duplicated().sum()
df.nunique()
```

### 4. Explore Categorical Data

```python
df["Gender"].unique()
df["Product Category"].unique()
df["Payment Method"].unique()
```

---

# 📈 Business Questions

This project answers the following questions:

### Basic Analysis

1. What is the total revenue?
total_revenue=df['Total Amount'].sum()
int(total_revenue)
3. What is the total number of transactions?
4. What is the total quantity sold?
5. What is the average transaction amount?
6. What is the highest transaction amount?
7. Which category generates the highest revenue?
8. Which category sells the highest quantity?
9. Which gender contributes the highest revenue?

### Customer Analysis

9. Who are the top 5 customers by spending?
10. What is the average spending per customer?
11. Which customers have spending above the overall average?
12. What is the most frequently purchased category for each gender?

### Product & Category Analysis

13. What is the average price per unit for each category?
14. Which is the most expensive category based on average price?
15. Which category has the highest average quantity per transaction?
16. What are the top 3 categories by revenue?
17. What percentage of total revenue does each category contribute?

### Age Analysis

18. What is the most common customer age?
19. Which age group generates the highest revenue?
20. Which age group spends the most within each gender?
21. What is the relationship between age and total spending?
22. What is the relationship between quantity and total amount?

### Time Analysis

23. What is the highest-revenue month?
24. What is the lowest-revenue month?
25. How does revenue change over time?
26. Which months have the highest number of transactions?

---

# 📊 Data Visualization

The project uses Matplotlib and Pandas visualization to create:

* Revenue by Product Category
* Quantity Sold by Category
* Sales by Gender
* Revenue by Age Group
* Monthly Revenue
* Daily Revenue
* Age vs Total Spending
* Quantity vs Total Amount
* Transaction Amount Distribution
* Transaction Amount by Category

Example:

```python
import matplotlib.pyplot as plt

category_revenue = df.groupby(
    "Product Category"
)["Total Amount"].sum()

category_revenue.plot(
    kind="bar",
    figsize=(10, 6),
    title="Revenue by Product Category",
    xlabel="Product Category",
    ylabel="Total Revenue"
)

plt.show()
```

---

# 🧹 Data Cleaning

The dataset was checked for:

* Missing values
* Duplicate records
* Incorrect data types
* Unique values
* Invalid values

Date conversion:

```python
df["Date"] = pd.to_datetime(df["Date"])
```

Age groups:

```python
bins = [0, 18, 30, 40, 50, 60, 100]

labels = [
    "Under 18",
    "18-30",
    "31-40",
    "41-50",
    "51-60",
    "60+"
]

df["Age Group"] = pd.cut(
    df["Age"],
    bins=bins,
    labels=labels
)
```

---

# 💡 Key Insights

The analysis helps identify:

* Best-performing product categories
* Highest-spending customers
* Customer purchasing behavior
* Gender-wise purchasing patterns
* Age-group spending patterns
* Monthly and daily revenue trends
* Relationship between quantity and spending
* Categories contributing most to overall revenue

---

# 📁 Project Structure

```text
Retail-Sales-Python-Analysis/
│
├── README.md
├── retail_sales_analysis.ipynb
├── retail_sales_dataset.csv
│
├── screenshots/
│   ├── revenue_by_category.png
│   ├── sales_by_gender.png
│   ├── monthly_revenue.png
│   └── age_vs_spending.png
│
└── requirements.txt
```

---

# 🎯 Skills Demonstrated

* Python
* Pandas
* NumPy
* Data Cleaning
* Exploratory Data Analysis (EDA)
* GroupBy Analysis
* Aggregation
* Sorting & Filtering
* Date & Time Analysis
* Correlation Analysis
* Data Visualization
* Business Problem Solving

---

# 🚀 Conclusion

This project demonstrates how Python and Pandas can be used to transform raw retail transaction data into meaningful business insights.

