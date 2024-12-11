# Gradient Boosting for Regression
[![Gradient Boosting](https://img.shields.io/badge/Gradient--Boosting-Regression--Friendly-blue?style=for-the-badge&logo=codefactor&logoColor=white)](https://scikit-learn.org/stable/modules/ensemble.html#gradient-boosting)


## Introduction

Gradient Boosting is a powerful ensemble machine learning technique widely used for both regression and classification tasks. By sequentially combining weak learners (typically decision trees), Gradient Boosting incrementally improves predictions by minimizing errors at each step.

This tutorial demonstrates how to:
1. Load and preprocess the Boston Housing Dataset.
2. Train a Gradient Boosting Regressor.
3. Evaluate the model's performance using Mean Squared Error (MSE) and R-squared (R²) metrics.
4. Analyze feature importance to understand which factors contribute most to predicting housing prices.

This approach builds on principles discussed by Friedman (2001) on Gradient Boosting machines, implemented here using the Scikit-learn library.

---
### Prerequisites
- [![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)

- [![Google Colab](https://img.shields.io/badge/Google%20Colab-Data%20Science%20Platform-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com/)


- Libraries:
  - ![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
  - [![matplotlib](https://img.shields.io/badge/matplotlib-008080?style=for-the-badge&logoColor=white)](https://matplotlib.org/)

  - [![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)

  - [![numpy](https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)


Install the required libraries using:
```bash
pip install -r requirements.txt
```

### Running the Notebook
1. Clone the repository:
   ```bash
   git clone https://github.com/sparkysparo/gradient-boosting-for-regression.git
   ```
2. Navigate to the `notebooks` folder:
   ```bash
   cd gradient-boosting-for-regression/notebooks
   ```
3. Launch Google Colab Notebook:
   ```bash
   Google Colab notebook
   ```
4. Open the `Gradient_Boosting_for_Regression_By_Paschal_Uzoegwu.ipynb` file and follow the instructions.
    
## Dataset Description

The Boston Housing Dataset contains 506 samples with 13 features and one target variable (`MEDV`, the median value of owner-occupied homes in $1000s). Key features include:
- **CRIM**: Per capita crime rate.
- **RM**: Average number of rooms per dwelling.
- **LSTAT**: Percentage of lower-status population.
- **DIS**: Weighted distance to five Boston employment centers.

This dataset is suitable for exploring relationships between socio-economic factors and housing prices. However, it’s important to note its limitations, such as outdated information and potential ethical concerns regarding bias in the data.

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
 These results indicate the model explained 92% of the variance in housing prices, showcasing strong predictive accuracy. However, further validation on external datasets is recommended to ensure generalizability.

### Feature Importance
The top three features influencing housing prices:
1. **RM** (Average Number of Rooms): 41.74%
2. **LSTAT** (Lower-Status Population): 37.43%
3. **DIS** (Weighted Distance to Employment Centers): 7.47%

---

## Accessibility Considerations

1. **Color-blind-friendly visuals**: Feature importance bar charts use distinguishable shades with text annotations.
2. **Screen reader compatibility**: Key outputs, such as model metrics and feature importance, are described in text.
3. **Concise formatting**: A structured format enhances readability for diverse audiences.
---

## Conclusion

Gradient Boosting is an effective machine learning technique for regression tasks, offering strong predictive performance and insights into feature importance. Using the Boston Housing Dataset, the model achieved a high R² score, demonstrating its ability to accurately predict housing prices. Key features such as RM, LSTAT, and DIS provide valuable insights into the factors influencing housing prices.The model's performance highlights its capability to predict housing prices effectively.

Recomendation For Future Work:
1.Comparing Gradient Boosting with other models like Random Forests or Neural Networks.
2. Exploring hyperparameter optimization techniques for improved performance.
3. Addressing biases and ethical concerns in the dataset.

By following this tutorial, readers will gain a solid understanding of how to apply Gradient Boosting for regression problems. For further details, refer to the foundational work by Friedman (2001) and Pedregosa et al. (2011).
---

## References

1. Friedman, J. H. (2001). *Greedy function approximation: A gradient boosting machine*. Annals of Statistics, 29(5), 1189-1232.
2. Pedregosa et al. (2011). *Scikit-learn: Machine Learning in Python*. Journal of Machine Learning Research, 12, 2825-2830.
3. Boston Housing Dataset: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Housing).


## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

