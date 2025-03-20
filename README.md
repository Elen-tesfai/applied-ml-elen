# Lab 03: Applied Machine Learning

In this lab, we explore data preprocessing and feature engineering techniques for a Titanic dataset. The steps include:

1. Data cleaning: Handling missing values and encoding categorical variables.
2. Feature engineering: Combining existing columns and creating new features.
3. Model training: Splitting the data and training machine learning models.

## Key Steps:
- **Feature Engineering**: Created new features by combining existing columns like `Pclass` and `Embarked`.
- **Data Preprocessing**: Handled missing values and encoded categorical variables.
- **Model Training**: Split the data into training and testing sets.

For further details, check out the notebook `ml03_Elen.ipynb`.
# Titanic Survival Prediction

## Introduction

In this project, machine learning models are built to predict the survival of passengers on the Titanic using the Titanic dataset. Several models, including Decision Tree, Support Vector Machine (SVM), and Neural Networks (NN), are trained, evaluated, and compared.

---

## Section 1. Import and Inspect the Data

### 1.1 Load Titanic Dataset
The Titanic dataset is loaded using the `seaborn` library. It contains information about passengers, including features like age, sex, class, and whether they survived.

---

## Section 2. Data Exploration and Preparation

### 2.1 Handle Missing Values
Missing values are handled by imputing missing entries for columns like `age` with the median value and `embark_town` with the mode.

---

## Section 3. Feature Selection and Justification

### 3.1 Choose Features and Target
The target variable is `survived`, while input features include combinations like `alone`, `age`, and `family_size` depending on the case.

### 3.2 Define X (features) and y (target)
Input features (`X`) are defined based on selected cases, and the target variable (`y`) is `survived`.

---

## Section 4. Train a Classification Model (Decision Tree)

### 4.1 Split the Data
The dataset is split into training and test sets using `StratifiedShuffleSplit` to ensure the distribution of the target variable is consistent.

### 4.2 Create and Train Model (Decision Tree)
A Decision Tree classifier is created and trained using the training data.

### 4.3 Predict and Evaluate Model Performance
Model predictions are made, and performance is evaluated based on metrics such as accuracy, precision, recall, and F1-score.

### 4.4 Report Confusion Matrix (as a heatmap)
The confusion matrix is visualized as a heatmap to help understand the model's predictions.

### 4.5 Report Decision Tree Plot
A plot of the decision tree is generated for visualization, showing how decisions are made based on the features.

### 4.6 Evaluate Model Performance for Different Input Features
The model performance is evaluated using different sets of features, such as `alone`, `age`, and `family_size`.

### Reflection 4: Model Performance Evaluation
This section reflects on how the model performed across different feature combinations, noting accuracy, recall, and precision.

### Explanation of Reflection 4: Model Performance Evaluation
The performance results are discussed, highlighting challenges such as class imbalance and suggestions for improvement.

---

## Section 5. Compare Alternative Models (SVC, NN)

### 5.1 Train and Evaluate Model (SVC)
The Support Vector Classifier (SVC) model is trained and evaluated using different kernels, including `RBF` and `Linear`.

### 5.2 Train and Evaluate Model (NN MLP)
The Neural Network model is trained and evaluated using the Multi-Layer Perceptron (MLP) classifier.

### Reflection 5: Model Performance Evaluation
The performance of each model is compared, and insights are drawn regarding which model performed best.

---

## Section 6. Final Thoughts & Insights

### 6.1 Summarize Findings
A summary of the findings, including the strengths and weaknesses of each model, and the most important features for prediction.

### 6.2 Discuss Challenges Faced
Challenges encountered during the project, such as class imbalance, overfitting, and missing data, are discussed.

### 6.3 Next Steps
Future steps include testing additional features, such as `Pclass` or `Embarked`, and improving model performance.

---

## Playing with Hyperparameters

Suggestions for experimenting with hyperparameters across different models to optimize performance.

---

## 7. Summary Table

A table summarizing the performance of all models, including accuracy, precision, recall, and F1-score for both classes (0: Non-survived, 1: Survived).

| Model                        | Accuracy | Precision (0) | Precision (1) | Recall (0) | Recall (1) | F1-Score (0) | F1-Score (1) | Key Observations                                      |
|------------------------------|----------|---------------|---------------|------------|------------|--------------|--------------|------------------------------------------------------|
| **Decision Tree**             | 75.65%   | 0.75          | 0.72          | 0.87       | 0.52       | 0.81         | 0.61         | Overfitting observed, strong for class 0, weak for class 1 |
| **Neural Network (MLP)**      | 74%      | 0.73          | 0.72          | 0.70       | 0.52       | 0.71         | 0.61         | Moderate improvement over Decision Tree, complexity increased |
| **SVM (RBF Kernel)**          | 67%      | 0.66          | 0.72          | 0.95       | 0.21       | 0.78         | 0.32         | Strong for non-survivors, poor recall for survivors    |
| **SVM (Linear Kernel)**       | 75%      | 0.77          | 0.71          | 0.86       | 0.57       | 0.81         | 0.63         | Balanced performance, higher accuracy than RBF         |
| **SVM (Polynomial Kernel)**   | 65%      | 0.64          | 0.71          | 0.97       | 0.12       | 0.77         | 0.20         | Struggles with recall for class 1, better for class 0   |
| **SVM (Sigmoid Kernel)**      | 61%      | 0.69          | 0.48          | 0.66       | 0.51       | 0.68         | 0.50         | Moderate overall performance, lowest accuracy         |

---