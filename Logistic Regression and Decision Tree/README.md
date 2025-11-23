# 📈 Analysis: Logistic Regression and Decision Tree

[View the Notebook: Logistic Regression and Decision Tree.ipynb](./Logistic%20Regression%20and%20Decision%20Tree.ipynb)

## Project Focus
The goal of this analysis was to build and compare supervised machine learning models for predicting customer churn.

* **Build a Logistic Regression model** to establish a baseline for binary classification.
* **Construct a Decision Tree model** to capture non-linear relationships and interpret decision rules.
* **Evaluate model performance** using standard metrics (Accuracy, Precision, Recall, F1-Score) and visualizations (ROC Curve, Confusion Matrix).
* **Optimize the Decision Tree** using Cost Complexity Pruning to prevent overfitting.

---

## 📝 Analysis Content Summary

The notebook covers the following key modeling operations:

### 1. Data Preprocessing
* **Encoding:** Converted categorical variables (`Geography`, `Gender`) into numerical format using One-Hot Encoding (`pd.get_dummies`).
* **Feature Selection:** Removed non-predictive identifier columns (`RowNumber`, `CustomerId`, `Surname`).
* **Scaling:** Applied `StandardScaler` to standardize numerical features, ensuring stable convergence for Logistic Regression.
* **Splitting:** Divided the dataset into 80% training and 20% testing sets to evaluate generalization.

### 2. Logistic Regression
* **Model Training:** Implemented a Logistic Regression classifier to predict churn probability.
* **Evaluation:** Assessed performance using a Confusion Matrix, Classification Report, and Bar Plot of metrics.
* **Visuals:** Plotted the ROC Curve (Receiver Operating Characteristic) and calculated the AUC score to measure class separation capability.

### 3. Decision Tree & Pruning
* **Initial Tree:** Trained a standard Decision Tree classifier and visualized the complex tree structure.
* **Cost Complexity Pruning:** Performed post-pruning analysis to find the optimal `ccp_alpha` parameter. This involved:
    * Calculating total impurity vs. effective alpha.
    * Plotting tree depth and node count against alpha values.
    * Comparing training vs. testing accuracy across different alphas to find the "sweet spot".
* **Optimized Model:** Built a final `clf_pruned` tree using the optimal alpha, resulting in a smaller, more interpretable model.

---

## 📂 Data Files Used

* **Dataset:** `Churn_Modelling.csv`