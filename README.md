# Customer Churn Prediction using Databricks Lakehouse

## Project Overview

Customer churn is a major challenge for telecom companies. When customers stop using a service, it directly impacts company revenue and growth. Businesses need data-driven solutions to identify customers who are likely to leave so they can take preventive actions.

This project builds an **end-to-end data engineering and machine learning pipeline** using the Databricks Lakehouse platform. The system processes raw telecom customer data using the **Medallion Architecture (Bronze → Silver → Gold)** and trains a machine learning model to predict customer churn.

The final output is a prediction system that helps telecom companies identify high-risk customers and improve retention strategies.

---

## Problem Statement

Telecommunication companies collect large volumes of customer data such as usage patterns, billing details, and service subscriptions. However, identifying customers who are likely to churn using traditional analysis methods is difficult.

The goal of this project is to design a **data pipeline and machine learning solution** that predicts whether a customer will churn using historical telecom data.

This system helps businesses take proactive actions such as:

- Offering personalized discounts
- Improving customer service
- Targeting retention campaigns

---

## Dataset

The dataset used in this project is the **Telco Customer Churn Dataset**.

It contains information about telecom customers including:

- Customer demographic details
- Account information
- Services subscribed
- Monthly billing data
- Contract details
- Customer churn status

Target variable: 

Values:
- Yes → Customer leaves the service
- No → Customer continues using the service

---

## Architecture Diagram

<p align="center">
  <img src="ChatGPT Image Mar 12, 2026, 10_43_52 PM.png" width="800"/>
</p>

This project follows the **Medallion Data Architecture**, which consists of three layers:

### Bronze Layer
Raw data ingestion layer.

- Stores original dataset
- No transformations applied
- Maintains raw historical data

### Silver Layer
Data cleaning and transformation layer.

Tasks performed:
- Handling missing values
- Data type conversions
- Removing inconsistencies
- Preparing structured datasets

### Gold Layer
Analytics and machine learning ready data.

Tasks performed:
- Feature engineering
- Creating aggregated datasets
- Preparing data for machine learning models

---

## Technology Stack

- Databricks
- Delta Lake
- MLflow
- Apache Spark
- PySpark
- SQL
- Python

---

## Data Pipeline Workflow

The pipeline consists of the following steps:

### 1. Data Ingestion
The telecom churn dataset is uploaded and stored as a Delta table in Databricks.

### 2. Bronze Layer
Raw data is stored in the Bronze table.


Values:
- Yes → Customer leaves the service
- No → Customer continues using the service

---

## Architecture Diagram

![Medallion Architecture](architecture/medallion_architecture.png)

This project follows the **Medallion Data Architecture**, which consists of three layers:

### Bronze Layer
Raw data ingestion layer.

- Stores original dataset
- No transformations applied
- Maintains raw historical data

### Silver Layer
Data cleaning and transformation layer.

Tasks performed:
- Handling missing values
- Data type conversions
- Removing inconsistencies
- Preparing structured datasets

### Gold Layer
Analytics and machine learning ready data.

Tasks performed:
- Feature engineering
- Creating aggregated datasets
- Preparing data for machine learning models

---

## Technology Stack

- Databricks
- Delta Lake
- MLflow
- Apache Spark
- PySpark
- SQL
- Python

---

## Data Pipeline Workflow

The pipeline consists of the following steps:

### 1. Data Ingestion
The telecom churn dataset is uploaded and stored as a Delta table in Databricks.

### 2. Bronze Layer
Raw data is stored in the Bronze table.


### 4. Gold Layer
Feature engineering is performed to create datasets suitable for machine learning.


---

## Machine Learning Pipeline

The machine learning pipeline includes:

1. Feature extraction from Gold layer
2. Train-test data split
3. Model training
4. Model evaluation
5. Prediction generation

### Model Used

Logistic Regression

This model predicts the probability of customer churn.

---

## Model Evaluation Metrics

The model performance is evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score

These metrics help measure the effectiveness of the churn prediction model.

---

## MLflow Experiment Tracking

MLflow is used to track machine learning experiments.

Tracked information includes:

- Model parameters
- Evaluation metrics
- Model versions
- Experiment runs

This helps manage and reproduce machine learning experiments efficiently.

---

## Prediction Pipeline

The trained model generates churn predictions for customers.

Predictions include:

- Customer churn probability
- Predicted churn class

The results are stored in the final prediction table.


---

## Business Insights

Based on the analysis, several insights can be observed:

- Customers with **month-to-month contracts** have higher churn rates.
- Customers with **higher monthly charges** tend to churn more frequently.
- Customers with **longer tenure** are less likely to churn.

These insights can help companies develop effective customer retention strategies.

---


---

## Future Improvements

Possible improvements for this project include:

- Implementing real-time data pipelines
- Deploying the model as an API service
- Creating dashboards for business users
- Using advanced machine learning models

---

## Author

Nandini Wadile  
Artificial Intelligence and Data Science Student

This project was developed as part of the **Build with Databricks Project Challenge - 2**.

