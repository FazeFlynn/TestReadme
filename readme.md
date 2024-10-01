# AIML Class Notes

---

## 29 August 2024

### Machine Learning

**Prerequisites:**
- Statistics and Probability

**Types of Machine Learning:**
1. **Supervised Learning:** 
   - Dependent (Target) and Independent (Features) variables.
2. **Unsupervised Learning:** 
   - Clustering of data.
3. **Reinforcement Learning:** 
   - Can involve both supervised and unsupervised elements. Commonly used in robotics, where the model learns through feedback from its actions.

**Types of Variables:**
1. **Numerical (Quantitative)**
2. **Categorical**
   - Unsure distinction between continuous and categorical, quantitative and qualitative, or discrete (whole numbers only).

---

## 31 August 2024

### Supervised Machine Learning

**Divided into:**
- **Regression:** Used when the target variable is continuous.
- **Classification:** Used when the target variable has a limited number of categories.

**Data Types:**
- **Training Data**
- **Testing Data**

**Types of Categorical Data:**
1. **Nominal Data**
2. **Ordinal Data**

**Note:** Check the **target (dependent variable)** to decide whether to use Regression or Classification:
- Continuous target → **Regression**
- Categorical target → **Classification**

> If the number of categories < 30 → Classification, otherwise Regression (usually decided by domain experts in companies).

---

### K-Nearest Neighbors (KNN)

**Handling Imbalanced Datasets:**
1. **Undersampling**
2. **Oversampling**
3. **SMOTE:** Synthetic Minority Over-sampling Technique to balance data by generating new samples near existing ones.

**Disadvantages of KNN:**
1. Not suitable for large datasets due to high computational complexity in calculating distances.
2. Sensitive to outliers, requiring a clean dataset.
3. Imbalanced datasets can reduce the efficiency and accuracy of the KNN algorithm.

**Distance Metrics:**
- **Euclidean Distance:** Shortest distance (based on Pythagoras' theorem).
- **Manhattan Distance:** Sum of the absolute differences along each axis.

**Train-Test Split:**
- `x_train`, `y_train`, `x_test`, `y_test`

---

## Exam Topics - 17 September 2024

**Units 1 and 2:**
- **Algorithms:** Linear Regression, KNN
- **Accuracy Metrics:** R-squared (R²) for regression, precision/recall for classification
- **Supervised, Unsupervised, and Reinforcement Learning**
- **Measures of Central Tendency:** Mean, Median, Mode
- **Types of Variables:** Numerical and Categorical, Interval Ratios
- **Statistics in Machine Learning**

---

## 17 September 2024

### Precision & R-Squared (for Regression)

1. **R-Squared (R²):**
   - Formula: 
     \[
     R^2 = 1 - \left(\frac{\text{Sum of Squared Residuals}}{\text{Total Sum of Squares}}\right)
     \]
   - Problem: It doesn't account for which features are relevant.

2. **Adjusted R-Squared:**
   - Formula:
     \[
     \text{Adjusted } R^2 = 1 - \left(\frac{(1-R^2)(N-1)}{N-P-1}\right)
     \]
   - `N`: Number of data points
   - `P`: Number of independent features

---

### Recall

**Fitting Models:**
- **Overfitting:** High train accuracy, but low test accuracy.
- **Underfitting:** Insufficient data to train the model.
- **Best Fitting:** Good accuracy for both train and test datasets.

**Errors:**
- **Bias:** Training errors.
- **Variance:** Testing errors.

---

## 18 September 2024

### Classification

| y (Actual) | ŷ (Predicted)  | 
|------------|----------------|
| 0          | 1              |
| 1          | 1              |
| 0          | 0              |
| 1          | 1              |
| 1          | 1              |
| 0          | 1              |
| 1          | 0              |

### Confusion Matrix:

|               | Actual 1 | Actual 0 |
|---------------|----------|----------|
| **Pred 1**    | TP = 3   | FP = 2   |
| **Pred 0**    | FN = 1   | TN = 1   |

---

## 19 September 2024

### Performance Metrics for Imbalanced Data

1. **Precision:**
   - Formula: 
     \[
     \text{Precision} = \frac{TP}{TP + FP}
     \]

2. **Recall:**
   - Formula: 
     \[
     \text{Recall} = \frac{TP}{TP + FN}
     \]
   - Used when reducing **False Negatives (FN)** is important.

3. **F-Beta Score:**
   - Combines precision and recall.
   - Formula: <img src="https://mathembed.online/embed/h4RiJxAv7X6VO4shtAen" alt="Mean Formula" width="100" height="auto" />
   <!-- - Formula: ![imgPika](https://islamkhan.in/img/webPikaPur.png) -->
   <!-- - Formula: -->




---

## 21 September 2024

### Descriptive and Inferential Statistics

#### Measures of Central Tendency:
1. **Mean:** 
   - Formula: 
     \[
     \text{Mean} = \frac{\text{Sum of All Numbers}}{\text{Count of Numbers}}
     \]
2. **Median:**
   - Arrange data in ascending order and pick the middle value.
   - Use **Median** when there are outliers.
3. **Mode:**
   - The most frequent value. Use Mode for categorical data.

#### Measures of Variance:
- **Variance:** Describes the spread of data around the mean.
- **Standard Deviation:** The square root of variance.

---

### KNN for Classification and Regression

1. **KNN for Classification:**

```bash
            |
            |     *   *
            |   * *  *    0   *  0
    Graph   |     *    *  0  X
            |    0    0    0   0        
            |   0 0     0    0
            |       0      
            -------------------------
```
