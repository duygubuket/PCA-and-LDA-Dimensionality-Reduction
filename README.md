# PCA-and-LDA-Dimensionality-Reduction

## 📌 Project Overview

This project performs a comparative analysis of classification methods — specifically **Quadratic Discriminant Analysis (QDA)** and **Linear Discriminant Analysis (LDA)** — on a two-class dataset. The goal is to understand how class distribution and covariance structures impact model performance and decision boundaries.

## 🔍 Summary of Results

### Class Distribution and Covariance

- The dataset consists of **two distinct classes** with some **overlap**, which limits perfect classification.
- **Class centers**:
  - Class 1 (Blue): approximately at (0.94, 2.00)
  - Class 2 (Orange): approximately at (2.99, 5.02)
- **Covariance patterns**:
  - Class 1 shows **higher variance in feature 2 (2.80)** than feature 1 (1.96), leading to a vertically stretched ellipse.
  - Class 2 exhibits a **strong negative correlation (-0.78)** between its features, leading to a tilted elliptical shape.

### QDA (Quadratic Discriminant Analysis)

- The **decision boundary is curved**, adapting to the class-specific covariance.
- **Training error**: 9.13%
- **Test error**: 9.00%
- The model appears to generalize well without overfitting.
- QDA effectively models the different shapes and orientations of class distributions.

### LDA (Linear Discriminant Analysis)

- Assumes **shared covariance** across classes, leading to a **linear decision boundary**.
- **Training error**: 10.13%
- **Test error**: 9.00%
- The **pooled covariance matrix** shows minimal feature correlation, which supports an axis-aligned boundary.
- LDA performs similarly to QDA in terms of test error, despite its simpler assumptions.

### Comparative Insights

- Both QDA and LDA achieve the **same test accuracy (9%)**, but QDA fits training data slightly better.
- The additional complexity of QDA yields a more flexible boundary, especially in regions with high curvature.
- In this case, the **simpler linear model (LDA)** is almost as effective as the more expressive QDA.

## 📄 License

This project is licensed under the [MIT License](LICENSE).
