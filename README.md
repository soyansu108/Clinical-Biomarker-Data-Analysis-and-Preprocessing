# Clinical Biomarker Data Analysis and Preprocessing Using Python

Analysis and preprocessing of clinical biomarker data using Python, Pandas, NumPy, and Matplotlib, with a focus on outlier handling, normalization, and standardization as preparation for machine learning.

## Project Overview

This project analyzes clinical and blood-related biomarker measurements to understand their distributions, identify and investigate potential outliers, handle unusual values using different approaches, and apply feature-scaling techniques.

The project uses a clinical biomarker dataset containing 116 observations and the following features:

- Age
- BMI
- Glucose
- Insulin
- HOMA
- Leptin
- Adiponectin
- Resistin
- MCP.1
- Classification

## What I Explored

### 1. Data Exploration

- Loaded the dataset using Pandas
- Inspected the data using `head()` and `describe()`
- Examined the distributions of the clinical measurements using Matplotlib

### 2. Outlier Detection

Potential outliers were investigated using the **Interquartile Range (IQR)** method.

The `MCP.1` feature contained several extreme values, so it was investigated in greater detail.

### 3. Outlier Handling

Three different approaches were explored:

**Outlier Removal**

The four observations with `MCP.1 = 1698.44` were removed from a copy of the original dataset, reducing the dataset from 116 to 112 observations.

**Log Transformation**

A natural logarithm transformation was applied to a separate copy of the original dataset. All 116 observations were retained while large `MCP.1` values were compressed.

**Outlier Capping**

Extreme `MCP.1` values were capped at the original upper IQR boundary instead of removing the observations. All 116 observations were retained.

These approaches were compared using boxplots and summary statistics.

### 4. Normalization

Min-Max normalization was applied to the clinical measurement features.

The features were rescaled to a range of **0 to 1**, making them more comparable in scale.

### 5. Standardization

Standardization was applied to the same clinical measurement features.

The resulting features were centered around **0**, with a standard deviation of **1**.

The normalized and standardized data were then visualized and compared to understand how the two scaling methods change the representation of the data.

## Key Learning Outcomes

- Learned to inspect and visualize clinical datasets using Pandas and Matplotlib
- Learned how the IQR method can identify potential outliers
- Explored multiple strategies for handling extreme values
- Learned that an outlier is not necessarily an error and should be investigated before removal
- Learned the difference between normalization and standardization
- Understood how feature scaling prepares numerical data for machine learning
- Gained practical experience with NumPy alongside Pandas and Matplotlib

## Tools and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Google Colab

## Files

- `Blood_Biomarker_Data_Analysis_&_Preprocessing.ipynb` — Complete analysis and preprocessing notebook
- `dataR2.csv` — Clinical biomarker dataset

## Conclusion

This project provided practical experience with data inspection, visualization, statistical outlier detection, outlier handling, normalization, and standardization. It demonstrates how different preprocessing methods can affect a dataset and provides a foundation for working with biological and clinical data in machine learning.
