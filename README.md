E-Commerce Product Sales — Exploratory Data Analysis (EDA)

An end-to-end Exploratory Data Analysis (EDA) project using Python to analyze product sales, pricing patterns, customer ratings, category performance, and relationships between key business metrics across 1,000 online retail transactions.

The project focuses on understanding sales behavior, validating data quality, identifying category-level patterns, and determining whether product price and customer ratings have a meaningful relationship with sales volume.

📌 Project Overview

Objective:
Analyze an e-commerce product sales dataset to identify important business patterns related to:

Product pricing
Units sold
Customer ratings
Category performance
Price distribution
Relationships between numerical variables
Data quality and consistency

The analysis uses statistical summaries and visualizations to transform raw sales data into actionable business insights.

📊 Dataset

Dataset: Pakistan_Online_Product_Sales.csv

Dimensions: 1,000 rows × 6 columns

Features
Column	Description
ProductID	Unique identifier for each product
ProductName	Product name/label
Category	Product category
Price	Product price in PKR
UnitsSold	Total number of units sold
Rating	Customer rating from 1.0 to 5.0
Product Categories
Books
Beauty
Home & Kitchen
Clothing
Sports
Electronics
🛠️ Tech Stack
Programming Language
Python
Environment
Jupyter Notebook
Libraries
Library	Purpose
Pandas	Data loading, cleaning and manipulation
NumPy	Numerical and mathematical operations
Matplotlib	Data visualization
Seaborn	Statistical visualization
Statsmodels	Statistical analysis and modeling support
🔎 Analysis Workflow
1. Data Ingestion

The dataset was imported into Python using Pandas.

import pandas as pd

df = pd.read_csv("Pakistan_Online_Product_Sales.csv")

Initial checks were performed to understand:

Dataset dimensions
Column names
Data types
Sample records
Numerical variables
2. Data Cleaning & Quality Assessment

The dataset was checked for missing values and duplicate records.

df.isnull().sum()
df.duplicated().sum()
Data Quality Results
Missing values: 0
Duplicate records: 0

This indicates that the dataset was complete and did not contain duplicate observations requiring removal.

3. Descriptive Statistics

Summary statistics were calculated for the numerical variables:

Price
Units Sold
Rating

The analysis included:

Mean
Median
Mode
Standard deviation
Minimum
Maximum
Quartiles

These statistics were used to understand the central tendency and variability of the dataset.

📈 Exploratory Data Analysis
Univariate Analysis
Price Distribution

The distribution of product prices was examined using:

Histogram
KDE plot
Box plot

Price Statistics:

Metric	Value
Minimum	PKR 122.70
Maximum	PKR 4,997.13
Mean	PKR 2,551.31
Median	PKR 2,586.94
Standard Deviation	PKR 1,423.73

The price distribution covers a broad range of products, with no major extreme outliers identified through the box plot analysis.

📊 Category Performance

Total units sold were aggregated by product category to identify which retail departments generated the highest sales volume.

Category Ranking by Units Sold
Books: >40,000 units
Electronics: >40,000 units
Beauty: High sales volume
Sports: High sales volume
Home & Kitchen: Moderate sales volume
Clothing: Moderate sales volume

Books and Electronics recorded the highest overall unit sales within the dataset.

💰 Category Pricing Analysis

Average product prices were calculated for each category.

Category	Average Price
Beauty	~PKR 2,766.50
Sports	~PKR 2,646.71
Clothing	~PKR 2,540.75
Electronics	~PKR 2,480.84
Books	~PKR 2,466.86
Home & Kitchen	~PKR 2,404.45

The average prices across categories are relatively balanced, although Beauty products have the highest average price while Home & Kitchen products have the lowest.

🔗 Correlation Analysis

A correlation matrix was created to examine the linear relationships between:

Price
Units Sold
Rating
Correlation Results
Variables	Correlation
Price vs Units Sold	0.01
Price vs Rating	0.00
Units Sold vs Rating	0.05
Interpretation

The correlations are close to zero, indicating very weak linear relationships among these variables within this dataset.

This suggests that:

Product price alone does not show a meaningful linear relationship with units sold.
Higher prices are not associated with higher or lower customer ratings.
Customer ratings show very little linear association with sales volume.

Important: Correlation measures linear association and does not establish causation. Other factors such as product type, promotions, brand, availability, marketing, and seasonality could influence sales.

📊 Visualizations

The project includes multiple visualizations to communicate the findings effectively:

1. Price Distribution

Histogram with KDE showing the distribution of product prices.

2. Price Box Plot

Used to identify the spread and potential outliers in product prices.

3. Category Sales

Bar chart comparing total units sold across product categories.

4. Category Pricing

Bar chart comparing average product prices across categories.

5. Correlation Heatmap

Heatmap showing relationships between numerical variables.

💡 Key Business Insights
1. Sales and Price

The correlation between price and units sold is approximately 0.01, indicating almost no linear relationship in this dataset.

2. Customer Ratings and Sales

The correlation between rating and units sold is approximately 0.05, suggesting that ratings alone do not explain differences in sales volume.

3. Category Performance

Books and Electronics generated the highest overall unit sales among the analyzed categories.

4. Pricing Structure

Average prices remain relatively close across categories, with Beauty having the highest average price and Home & Kitchen the lowest.

5. Data Quality

The dataset contains no missing values and no duplicate records, making it suitable for exploratory analysis.



