# Gradient Boosting for Regression

## Introduction

Gradient Boosting is a powerful ensemble machine learning technique widely used for both regression and classification tasks. By sequentially combining weak learners (typically decision trees), Gradient Boosting incrementally improves predictions by minimizing errors at each step.

This tutorial demonstrates how to:
1. Load and preprocess the Boston Housing Dataset.
2. Train a Gradient Boosting Regressor.
3. Evaluate the model's performance using Mean Squared Error (MSE) and R-squared (R²) metrics.
4. Analyze feature importance to understand which factors contribute most to predicting housing prices.

The approach builds on principles discussed by Friedman (2001), implemented using the Scikit-learn library.

---
### Prerequisites
- Python 3.8+
- Jupyter Notebook
- Libraries:
  - scikit-learn
  - matplotlib
  - pandas
  - numpy
    
## Dataset Description

The Boston Housing Dataset contains 506 samples with 13 features and one target variable (`MEDV`, the median value of owner-occupied homes in $1000s). Key features include:
- **CRIM**: Per capita crime rate.
- **RM**: Average number of rooms per dwelling.
- **LSTAT**: Percentage of lower-status population.
- **DIS**: Weighted distance to five Boston employment centers.

This dataset is commonly used to predict housing prices based on these features.

---

## Methods Used

### Step 1: Data Preparation
- Split the dataset into training and testing sets (80:20 ratio) to ensure robust evaluation.

### Step 2: Model Training
- Algorithm: Gradient Boosting Regressor
- Hyperparameters:
  - Number of estimators: 100
  - Learning rate: 0.1
  - Maximum depth: 3
- These hyperparameters balance performance and computational efficiency, as suggested by Pedregosa et al. (2011).

### Step 3: Evaluation Metrics
- **Mean Squared Error (MSE)**: Measures the average squared difference between actual and predicted values.
- **R-squared (R²)**: Indicates how well the model explains variability in the target variable.

### Step 4: Feature Importance Analysis
- Computed and visualized feature importance scores to identify the most influential predictors of housing prices.

---

## Results

### Evaluation Metrics
- **Mean Squared Error (MSE)**: 6.21
- **R-squared (R²)**: 0.92  
  These metrics indicate a strong model fit, explaining 92% of the variability in housing prices.

### Feature Importance
The top three features influencing housing prices:
1. **RM** (Average Number of Rooms): 41.74%
2. **LSTAT** (Lower-Status Population): 37.43%
3. **DIS** (Weighted Distance to Employment Centers): 7.47%

---

## Accessibility Considerations

1. **Color-blind-friendly visuals**: Feature importance bar charts use distinguishable shades with text annotations.
2. **Screen reader compatibility**: Key outputs, such as model metrics and feature importance, are described in text.

---

## Conclusion

Gradient Boosting is an effective machine learning technique for regression tasks, offering strong predictive performance and insights into feature importance. The Boston Housing Dataset results demonstrate its ability to predict housing prices accurately, with key features like `RM`, `LSTAT`, and `DIS` providing valuable insights.

---

## References

1. Friedman, J. H. (2001). *Greedy function approximation: A gradient boosting machine*. Annals of Statistics, 29(5), 1189-1232.
2. Pedregosa et al. (2011). *Scikit-learn: Machine Learning in Python*. Journal of Machine Learning Research, 12, 2825-2830.
3. Boston Housing Dataset: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Housing).


## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

