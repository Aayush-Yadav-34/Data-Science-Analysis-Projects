# 📉 Analysis: Principal Component Analysis (PCA)

[View the Notebook: Principal Component Analysis (PCA).ipynb](./Principal%20Component%20Analysis%20(PCA).ipynb)

## Project Focus
The goal of this analysis was to implement dimensionality reduction techniques to simplify complex financial datasets while retaining essential information.

* **Perform PCA** to reduce the number of features in the dataset.
* **Evaluate Explained Variance** to automatically determine the optimal number of principal components.
* **Handle Non-Linear Data** using Kernel PCA methods on specific price metrics.
* **Maximize Class Separability** using Linear Discriminant Analysis (LDA) with stock index targets.
* **Visualize** the impact of dimensionality reduction on data distribution.

---

## 📝 Analysis Content Summary

The notebook covers four distinct operations:

### 1. Standard Principal Component Analysis (PCA)
* **Data Prep:** Dropped non-numeric columns ('Date', 'Stock Index') and applied `StandardScaler` to normalize the remaining financial indicators.
* **Variance Retention:** Configured PCA to retain 99% of the variance, which successfully reduced the dataset dimensionality from **22 features to 19 principal components**.

### 2. Kernel PCA for Linearly Inseparable Data
* **Targeted Reduction:** Applied `KernelPCA` specifically to the 'Open Price' and 'Close Price' columns.
* **Non-Linear Mapping:** Used an "rbf" (Radial Basis Function) kernel with a gamma of 15 to project these features into a higher-dimensional space for better separability, reducing 2 features into 1 component.

### 3. Linear Discriminant Analysis (LDA)
* **Supervised Reduction:** Used 'Stock Index' as the target variable to find component axes that maximize the separation between different index classes.
* **Extreme Reduction:** Demonstrated the capability to compress **22 features down to just 1 component** while maintaining significant discriminatory power.

### 4. Data Visualization
* **Comparison:** Generated side-by-side scatter plots to compare the data distribution before and after PCA.
* **2D Projection:** Projected the high-dimensional scaled data onto 2 components to visually analyze the structure and variance retention.

---

## 📂 Data Files Used

* **Dataset:** `finance_economics_dataset.csv`