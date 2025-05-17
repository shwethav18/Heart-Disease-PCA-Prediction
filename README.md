# Heart Disease Prediction using EDA and PCA

This project analyzes the Cleveland Heart Disease dataset using exploratory data analysis (EDA) and Principal Component Analysis (PCA) to identify patterns and improve diagnostic modeling. The project focuses on uncovering hidden structures in the data and using dimensionality reduction to simplify and improve model performance.

## Dataset

- **Source:** Cleveland Heart Disease Dataset
- **Observations:** 297 rows (after removing missing data)
- **Variables:** Includes age, sex, chest pain type, cholesterol, max heart rate, ST depression, thalassemia, and diagnosis

## Objectives

- Explore patterns among clinical variables using EDA
- Use PCA to reduce dimensionality while preserving variance
- Use PCA components for predictive modeling of heart disease diagnosis

## Do We Need PCA?

Although most numeric variables in the dataset showed weak correlations (between 0 and 0.39), PCA was still valuable for:

- **Reducing dimensionality**: Even with low correlation, PCA helps compress multivariate data into fewer components.
- **Simplifying the feature space**: Especially useful for visualizations or quick diagnostics.
- **Improving interpretability and efficiency**: For models that benefit from reduced noise and redundancy.

PCA was justified based on:
- **Scree plot** suggesting 2–4 meaningful components
- **Kaiser Criterion** recommending 2 components
- **90% variance rule** supporting 4 components for predictive modeling

## Approach

1. **Data Cleaning**
   - Removed rows with missing `Thalassemia` values
   - Encoded target as binary: 0 = no disease, 1 = presence of disease
   - Normalized numeric features

2. **Exploratory Data Analysis**
   - Distribution plots for numerical features
   - Correlation heatmaps to detect redundancy
   - Identified clinical indicators of heart disease

3. **Principal Component Analysis (PCA)**
   - Scree plot and Kaiser Criterion used to determine number of components
   - Retained 4 components (explaining 90% variance)
   - Biplots used to interpret variable contributions

4. **Classification**
   - Logistic regression on PCA features
   - Evaluation metrics:
     - Sensitivity: 65.52%
     - Specificity: 80.60%
     - Precision: 76%
   - Highlighted potential for false negatives

## Transferable Skills Demonstrated

- Data wrangling and EDA
- Dimensionality reduction using PCA
- Interpretation of principal components
- Predictive modeling using logistic regression
- Critical reasoning on when and why to apply dimensionality reduction

## Future Improvements

- Apply oversampling or undersampling to balance classes
- Include lifestyle variables or genetic data for richer features
- Try ensemble models for improved accuracy
- Develop a visual tool using Streamlit or Tableau

## Tools Used

- Python (Pandas, NumPy, scikit-learn, matplotlib, seaborn)
- PCA and logistic regression from `sklearn`
- Jupyter Notebook for reproducibility
