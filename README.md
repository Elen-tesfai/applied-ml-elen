# Titanic Dataset Analysis

## Introduction

In this project, we analyze the Titanic dataset to predict the survival of passengers aboard the RMS Titanic. The dataset consists of several features such as age, sex, passenger class, fare, etc., and we aim to explore and transform these features to build a predictive model for passenger survival.

---

## Project Overview

This project is divided into several key sections:

### Section 1: Import and Inspect the Data

1. **Load the Dataset and Display the First 10 Rows**  
   We will start by loading the Titanic dataset and displaying the first few rows to understand its structure.

2. **Check for Missing Values and Display Summary Statistics**  
   We will check for any missing data and provide summary statistics, helping us understand the distribution and potential issues in the dataset.

### Section 2: Data Exploration and Preparation

1. **Explore Data Patterns and Distributions**  
   We will visualize the data to identify patterns, anomalies, or potential predictors, including creating histograms and scatter plots.

2. **Handle Missing Values and Clean Data**  
   We will address any missing values in the dataset and clean the data, including imputing missing values where necessary.

3. **Feature Engineering**  
   We will create new features or modify existing features to enhance the predictive power of the model. For example, combining `sibsp` and `parch` to create a `family_size` feature.

### Section 3: Feature Selection and Justification

1. **Choose Features and Target**  
   We will choose the most relevant input features and select the target variable, `survived`, to predict the likelihood of passenger survival.

2. **Define X and y**  
   We will define the feature matrix `X` (input features) and the target vector `y` (survival status).

### Section 4: Splitting

1. **Basic Train/Test Split**  
   We will split the dataset into training and testing subsets to evaluate the model's performance.

2. **Stratified Train/Test Split**  
   A stratified split ensures that the distribution of the target variable is similar in both the training and test datasets, improving model performance.

---

## Technologies Used

- Python 3.x
- Jupyter Notebooks
- Pandas, NumPy
- Matplotlib, Seaborn (for data visualization)
- Scikit-learn (for machine learning models and evaluation)

---

## Requirements

- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

To install the required dependencies, you can use the following:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
## How to Run the Project
```
1. **Navigate to the lab02 folder:**

```bash
   cd applied-ml-elen/lab02
``` 
2. **Open the Jupyter notebook:**

jupyter notebook ml02_elen.ipynb

3. **Follow the steps in the notebook to explore, preprocess, and build the model.**

This format separates each step clearly and is easy to follow when reading.