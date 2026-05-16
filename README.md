# aqi-risk-classification-svm-parallel-computing
Machine learning and parallel computing project classifying urban air quality risk using pollutant sub-indices, SVM modelling, and parallelised hyperparameter tuning in R.
# Urban Air Quality Risk Classification using SVM and Parallel Computing

## Project Summary

This project applies machine learning and parallel computing techniques to classify urban air quality risk using pollutant sub-index data and geographic features.

The aim was to build a predictive classification model that can assign air quality observations into risk categories, while also comparing standard machine learning execution with a parallelised hyperparameter tuning approach.

The project was completed as part of my MSc Data Science and Analytics coursework and demonstrates practical skills in data preprocessing, classification modelling, model evaluation, R programming, and high-performance computing concepts.

---

## Problem Statement

Air pollution is a major public health and environmental issue. Cities and countries need reliable ways to monitor air quality risk levels so that decision-makers can prioritise interventions, identify high-risk locations, and respond to hazardous pollution conditions.

The problem addressed in this project was:

> Can pollutant sub-index values and geographic information be used to classify urban air quality risk categories accurately, and can parallel computing improve the efficiency of model tuning?

---

## Why This Project Matters

Air quality classification is useful because decision-makers often need simple risk categories rather than raw pollutant values.

For example, instead of only seeing separate values for pollutants such as PM2.5, PM10, NO2, CO, and Ozone, a classification model can help identify whether an observation belongs to a low-risk, moderate-risk, unhealthy, or hazardous air quality category.

This project also matters from a technical perspective because model tuning can become computationally expensive as datasets and parameter grids grow. By comparing sequential and parallel grid search, the project shows how parallel computing can reduce runtime while maintaining model performance.

---

## Tools and Technologies Used

- **R**
- **RMarkdown**
- **Support Vector Machine**
- **Parallel computing in R**
- **Data preprocessing**
- **Exploratory data analysis**
- **Classification modelling**
- **Confusion matrix analysis**
- **Accuracy and F1-score evaluation**
- **Grid search hyperparameter tuning**

---

## Dataset

The project used an air quality dataset containing city-level air pollution and location-based information.

The dataset included:

- Air Quality Index values
- Pollutant sub-indices
- City and country information
- Latitude and longitude
- Air quality category labels

The original dataset contained approximately:

- **16,695 observations**
- **Around 175 countries**
- Multiple pollutant-related variables used for classification

A small sample dataset is included in the `data/` folder for demonstration purposes. The full dataset should not be uploaded publicly unless the licensing terms allow redistribution.

---

## Methodology

The project followed a standard machine learning workflow.

### 1. Data Understanding

The dataset was inspected to understand:

- Number of observations and variables
- Target class distribution
- Missing values
- Pollutant sub-index features
- Geographic features
- Air quality risk categories

### 2. Data Preprocessing

The preprocessing stage included:

- Cleaning missing or invalid values
- Selecting relevant predictor variables
- Encoding the target variable
- Preparing the dataset for classification
- Splitting the data into training and testing sets

### 3. Exploratory Data Analysis

Exploratory analysis was used to understand:

- Distribution of air quality risk categories
- Pollutant patterns across observations
- Class imbalance in the target variable
- Potential difficulty in predicting rare hazardous categories

### 4. Baseline SVM Model

A baseline Support Vector Machine model was trained to classify air quality risk categories.

The model was evaluated using:

- Accuracy
- Confusion matrix
- Per-class performance
- F1-score analysis

### 5. Hyperparameter Tuning

Grid search was applied to improve SVM performance by testing different parameter combinations.

The tuning process compared:

- Sequential grid search
- Parallel grid search

### 6. Parallel Computing Comparison

The parallel version of grid search was used to reduce runtime by distributing parameter search tasks across multiple workers/cores.

This allowed the project to compare:

- Model accuracy
- Runtime efficiency
- Speed-up achieved through parallel processing

---

## Key Results

The project achieved strong classification performance using SVM modelling.

Key results included:

- Baseline SVM model achieved high test accuracy.
- Tuned SVM improved classification performance after hyperparameter optimisation.
- Parallel grid search reduced tuning runtime significantly compared with sequential grid search.
- Sequential grid search runtime was approximately **25.68 seconds**.
- Parallel grid search runtime was approximately **6.92 seconds**.
- The parallel approach achieved approximately **3.7× speed-up**.
- Tuned SVM accuracy reached approximately **98.89%**.

These results show that the model was effective for air quality risk classification and that parallel computing improved the efficiency of the tuning process.

---

## Screenshots to Include

The following screenshots should be added to the `screenshots/` folder and displayed in this README.

### 1. Project Workflow

Add a simple diagram showing:

```text
Dataset → Preprocessing → EDA → Baseline SVM → Tuned SVM → Parallel Grid Search → Evaluation
