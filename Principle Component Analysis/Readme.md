# 📊✨ PCA Visualization Experiment (3D → 2D)



This project demonstrates **Principal Component Analysis (PCA)** step by step on synthetic 3D data.  
We generate two Gaussian-distributed classes, visualize them in 3D, compute PCA, plot eigenvectors, and finally reduce the data to 2D.

---

## 📌 Objectives
1. Generate synthetic 3D dataset (two classes).
2. Visualize data distribution in **3D scatter plots**.
3. Standardize features and compute **Covariance Matrix**.
4. Perform **Eigen Decomposition** to find principal components.
5. Plot eigenvectors (principal directions) in 3D space.
6. Project data onto **first two principal components (PC1 & PC2)**.
7. Visualize 2D representation of data with Plotly.

---

## 🛠️ Tech Stack
- **Python 3.12+**
- [NumPy](https://numpy.org/) → for data generation & matrix operations
- [Pandas](https://pandas.pydata.org/) → data handling
- [Plotly](https://plotly.com/python/) → interactive 3D & 2D scatter plots
- [Matplotlib](https://matplotlib.org/) → 3D eigenvector visualization
- [scikit-learn](https://scikit-learn.org/) → feature scaling (`StandardScaler`)

---

## 📂 Workflow

### **Step 1: Data Generation**
- Two classes are sampled from **multivariate Gaussian distributions**:
  - Class 1 → mean `[0, 0, 0]`
  - Class 2 → mean `[1, 1, 1]`
- Both use identity covariance matrix.
- Combined dataset → 40 samples, 3 features, labeled as `target`.

```python
mu_vec1 = np.array([0,0,0])
mu_vec2 = np.array([1,1,1])
cov_mat = np.eye(3)

