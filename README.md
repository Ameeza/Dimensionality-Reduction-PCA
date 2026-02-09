# Dimensionality-Reduction-PCA
### Project Overview

This project demonstrates how **Principal Component Analysis (PCA)** can be used for dimensionality reduction on the MNIST/Digits dataset and how it affects the performance of a **Logistic Regression** classifier. The goal is to reduce the number of features while retaining most of the important information and compare the model accuracy before and after dimensionality reduction.

---

### Dataset Used

* **Dataset**: MNIST / Digits dataset from `sklearn.datasets`
* **Description**: Handwritten digit images (0–9)
* **Original Feature Size**:

  * Each image is flattened into a 1D feature vector before processing.

---

### Steps Performed

1. **Load Dataset**

   * The digits dataset is loaded and images are flattened into feature vectors.

2. **Feature Scaling**

   * StandardScaler is applied to normalize the data.
   * This step is important because PCA is sensitive to feature scaling.

3. **Apply PCA**

   * PCA is applied with different numbers of components:
     **2, 10, 30, and 50**
   * Dimensionality reduction is performed on the scaled data.

4. **Explained Variance Analysis**

   * Explained variance ratio is calculated for each PCA setting.
   * Cumulative variance is plotted to understand how many components are needed to retain most of the information.

5. **Choosing Optimal Components**

   * From the cumulative variance plot, an optimal number of components can be selected based on variance retention (e.g., ~95%).

6. **Data Transformation**

   * The original dataset is transformed into a reduced-dimensional dataset using PCA.

7. **Model Training**

   * Logistic Regression is trained on:

     * Original (non-PCA) dataset
     * PCA-reduced dataset

8. **Model Comparison**

   * Accuracy of Logistic Regression is compared between:

     * Original feature space
     * Reduced feature space

9. **Visualization**

   * A 2D scatter plot using PCA with 2 components is plotted.
   * This helps visualize class separation among digit classes.

---

### Results

* **Original Dataset Accuracy**:
  Logistic Regression performs well but uses a high-dimensional feature space.

* **Reduced Dataset Accuracy**:
  Accuracy remains close to the original model while using significantly fewer features.

* **Observation**:
  PCA effectively reduces dimensionality with minimal loss in classification performance, making the model more efficient.

---

### Visual Outputs

* Cumulative Explained Variance Plot
* PCA 2D Scatter Plot showing digit class separation

---

### Conclusion

This experiment shows that PCA is a powerful technique for reducing dimensionality while preserving important information. Using PCA before training a classifier like Logistic Regression can improve efficiency and maintain good accuracy, especially for high-dimensional datasets like image data.

---

### Technologies Used

* Python
* NumPy
* Matplotlib
* Scikit-learn

---
