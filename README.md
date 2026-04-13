# 🧠 Machine Learning Comprehensive Notes

A structured guide covering the fundamental concepts, algorithms, and workflows of Machine Learning.

---

## 1. Introduction to Machine Learning
Machine Learning (ML) is the field of study that gives computers the ability to learn without being explicitly programmed. It focuses on the development of computer programs that can access data and use it to learn for themselves.

### **The Three Main Types**
1. **Supervised Learning:** The model learns from labeled training data (Input + Output).
2. **Unsupervised Learning:** The model finds hidden patterns or intrinsic structures in input data (No Labels).
3. **Reinforcement Learning:** An agent learns to make decisions by performing actions in an environment to maximize rewards.

---

## 2. Supervised Learning: Regression & Classification

### **A. Regression (Predicting Continuous Values)**
* **Linear Regression:** Fits a straight line to the data points.
    * **Formula:** $y = mx + c$
    * **Cost Function (MSE):** $J(\theta) = \frac{1}{2m} \sum_{i=1}^{m} (h_\theta(x^{(i)}) - y^{(i)})^2$
* **Polynomial Regression:** Used when data points do not follow a linear trend; uses a curve to fit data.

### **B. Classification (Predicting Categories)**
* **Logistic Regression:** Despite the name, it's used for binary classification. It uses the **Sigmoid Function** to map values between 0 and 1.
    * $\sigma(z) = \frac{1}{1 + e^{-z}}$
* **Decision Trees:** A flowchart-like structure where each internal node represents a "test" on an attribute.
* **Support Vector Machines (SVM):** Finds the optimal hyperplane that maximizes the margin between two classes.
* **K-Nearest Neighbors (KNN):** Classifies a data point based on how its neighbors are classified.

---

## 3. Unsupervised Learning: Clustering & Association

### **A. Clustering**
* **K-Means Clustering:** Groups data into $K$ number of clusters by calculating the distance between points and centroids.
* **Hierarchical Clustering:** Creates a tree of clusters (Dendrogram).

### **B. Dimensionality Reduction**
* **PCA (Principal Component Analysis):** Reduces the number of variables in a dataset while preserving as much information as possible.

---

## 4. Model Evaluation & Optimization

### **Overfitting vs. Underfitting**
* **Underfitting (High Bias):** The model is too simple and fails to capture the pattern (Low accuracy on both Train and Test sets).
* **Overfitting (High Variance):** The model learns the noise in the training data (High Train accuracy, Low Test accuracy).

### **Evaluation Metrics**
| Category | Metric | Description |
| :--- | :--- | :--- |
| **Regression** | **MAE** | Mean Absolute Error (Average of errors). |
| **Regression** | **RMSE** | Root Mean Squared Error (Penalizes larger errors). |
| **Classification** | **Accuracy** | Total correct predictions / Total predictions. |
| **Classification** | **Precision** | Quality of positive predictions. |
| **Classification** | **Recall** | Ability to find all positive instances. |
| **Classification** | **F1-Score** | Balance between Precision and Recall. |

---

## 5. The Machine Learning Workflow
1.  **Data Collection:** Gathering the raw data.
2.  **Data Cleaning:** Handling missing values, outliers, and duplicates.
3.  **Feature Engineering:** Selecting and transforming variables (Scaling, Encoding).
4.  **Model Selection:** Choosing the right algorithm for the problem.
5.  **Training:** Feeding data into the model.
6.  **Testing/Evaluation:** Checking performance on unseen data.
7.  **Hyperparameter Tuning:** Adjusting settings (like Learning Rate) to optimize the model.

---

## 6. Popular Libraries
* **NumPy / Pandas:** Data manipulation and matrix operations.
* **Scikit-Learn:** The go-to library for traditional ML algorithms.
* **Matplotlib / Seaborn:** Data visualization.
* **TensorFlow / PyTorch:** Deep Learning and Neural Networks.

---
# 🤖 Machine Learning Algorithms: A Deep Dive

This document explains the logic behind the algorithms implemented in this repository.

---

## 1. Linear Regression (Regression)
Used for predicting a continuous numerical value.
* **Core Idea:** Finds the "Line of Best Fit."
* **Equation:** $y = \beta_0 + \beta_1x$
* **Goal:** Minimize the **Mean Squared Error (MSE)**.

## 2. Logistic Regression (Classification)
Despite the name, it is used for classification (Yes/No, Spam/Not Spam).
* **Core Idea:** Uses the **Sigmoid Function** to squash any real-valued number into a range between 0 and 1.
* **Output:** A probability. If $> 0.5$, it's Class A; otherwise, Class B.

## 3. Decision Trees (Classification & Regression)
A tree-like model of decisions.
* **Core Idea:** Splits the data into subsets based on the most significant feature.
* **Metric:** Uses **Gini Impurity** or **Entropy** to decide where to "split" the branch.

## 4. K-Nearest Neighbors (KNN)
A "lazy" learning algorithm.
* **Core Idea:** To predict a new point, it looks at the $K$ closest points in the training data.
* **Logic:** "Tell me who your neighbors are, and I'll tell you who you are."

## 5. K-Means Clustering (Unsupervised)
Groups unlabeled data into $K$ clusters.
* **Core Idea:** Randomly picks $K$ centroids, assigns points to the nearest one, and then updates the centroid position until the clusters are stable.

## 6. Principal Component Analysis (PCA)
A dimensionality reduction technique.
* **Core Idea:** Reduces the number of features (columns) while keeping the most important information (variance) intact.
* **Use Case:** Speeding up training and visualizing high-dimensional data.

---

### 🚀 Implementation Checklist
For every algorithm in this repo, ensure you have:
1.  **Data Scaling:** Most ML models (like KNN/SVM) require features to be on the same scale (StandardScaler).
2.  **Train-Test Split:** Never evaluate a model on the same data it learned from.
3.  **Cross-Validation:** To ensure the model generalizes well to new data.

---
