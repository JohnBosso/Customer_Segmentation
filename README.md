# Customer Segmentation Classification Model

## Project Overview

This project is focused on building a classification model for customer segmentation based on online retail data. The goal is to categorize customers into different value segments using features like recency, frequency, and total sales. These segments are defined as:
- High-value customers
- Medium-value customers
- Low-value customers

The model leverages a K-Nearest Neighbors (KNN) classifier for predicting the customer segments.

## Data Source

The data used in this project is from the [Online Retail II](https://archive.ics.uci.edu/ml/datasets/Online+Retail+II) dataset, which contains transactional data from a UK-based online retailer.

### Dataset Columns:
- `InvoiceDate`: Date and time of the transaction.
- `Description`: Description of the item sold.
- `Quantity`: Quantity of items purchased.
- `Price`: Price of the item sold.
- `Country`: Country of the customer.
- `Customer ID`: Unique identifier for the customer.

## Steps Involved

1. **Data Cleaning**: 
   - Remove missing values.
   - Filter out negative and zero quantities.

2. **Feature Engineering**:
   - Extract `Year` and `Month` from `InvoiceDate`.
   - Calculate `Total Sales` as the product of `Quantity` and `Price`.
   - Aggregate data to compute customer-level features: 
     - Recency: Days since the last purchase.
     - Frequency: Total number of purchases.
     - Monetary: Total sales.

3. **Customer Segmentation**:
   - Label customers as "High_value", "Medium_value", or "Low_value" based on recency, frequency, and monetary features.

4. **Model Training**:
   - Apply a K-Nearest Neighbors (KNN) classifier to predict customer segments.

5. **Clustering**:
   - Apply K-Means clustering to further segment customers.

6. **Evaluation**:
   - Evaluate the classification model's performance using accuracy, classification report, and ROC curve.

## Key Python Libraries Used

- `pandas` for data manipulation
- `matplotlib` and `seaborn` for data visualization
- `scikit-learn` for machine learning tasks (KNN, KMeans, scaling, splitting data)

