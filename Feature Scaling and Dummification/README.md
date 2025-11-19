# 📈 Analysis: Feature Scaling and Dummification

[View the Notebook: Feature Scaling and Dummification.ipynb](./Feature%20Scaling%20and%20Dummification.ipynb)

## Project Focus
The goal of this analysis was to master essential data preprocessing techniques for machine learning, focusing on transforming numerical and categorical data into formats suitable for modeling.

* Apply various feature scaling techniques to standardize numerical ranges.
* Implement dummification (encoding) to convert categorical variables into numerical representations.
* Handle data quality issues such as missing values and class imbalance.

---

## 📝 Analysis Content Summary

The notebook covers the following key data science operations:

### Handling Numerical Data
* **Rescaling:** Transforms features to a specific range (0 to 1) using `MinMaxScaler`.
* **Standardization:** Applies Z-Score standardization (`StandardScaler`) and Robust scaling (`RobustScaler`) to handle outliers.
* **Normalization:** Scales individual observations to a unit norm using `Normalizer`.
* **Clustering:** Groups observations using `KMeans` clustering based on numerical features like Age and Balance.
* **Imputation:** Fills missing numerical values using `SimpleImputer`.

### Handling Categorical Data & Imbalanced Classes
* **One-Hot Encoding:** Converts nominal features (e.g., 'marital') into binary matrices using `LabelBinarizer`.
* **Dictionary Vectorization:** Transforms feature dictionaries into vectors using `DictVectorizer`.
* **Ordinal Encoding:** Bins continuous features (e.g., 'age') into logical groups (Young, Middle, Senior) and maps them to numeric values.
* **KNN Imputation:** Predicts and fills missing categorical values using `KNeighborsClassifier`.
* **Class Balancing:** Addresses target variable imbalance by downsampling the majority class.

---

## 📂 Data Files Used

All required data files (specifically `bank.csv`) are located in the parent **`../Datasets/`** folder.
