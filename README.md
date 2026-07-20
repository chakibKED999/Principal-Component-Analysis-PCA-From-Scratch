# 📊 Principal Component Analysis (PCA) From Scratch

> A complete implementation of Principal Component Analysis (PCA) using NumPy for multivariate data analysis. The project includes dimensionality reduction, inertia analysis, cosine quality (Cos²), contributions, correlation circles, biplots, and graphical interpretation of both individuals and variables.

![Python](https://img.shields.io/badge/Python-3.10-blue)
![NumPy](https://img.shields.io/badge/NumPy-Linear_Algebra-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-lightblue)
![PCA](https://img.shields.io/badge/Principal_Component_Analysis-ACP-red)
![Master](https://img.shields.io/badge/Master-MIV-lightgrey)

---

# 📖 Overview

This project presents a complete implementation of **Principal Component Analysis (PCA)** from scratch using only the scientific Python ecosystem.

Unlike implementations relying on machine learning libraries such as Scikit-Learn, every mathematical step of PCA is explicitly implemented, allowing a deeper understanding of the algorithm and its statistical foundations.

The project studies both:

- 👥 The cloud of individuals
- 📈 The cloud of variables

through multiple statistical indicators and graphical representations.

Several visualizations are generated, including:

- Principal Component Maps
- Correlation Circles
- Biplots
- Inertia Graphs
- Eigenvalue Analysis

This work was developed as part of the **Data Analysis** module in the **Master's Program in Image Processing & Artificial Intelligence (MIV)** at **USTHB**.

---

# ✨ Features

- 📊 PCA implementation from scratch
- 🧮 Matrix standardization
- 📈 Correlation matrix computation
- 🧠 Eigenvalue & Eigenvector decomposition
- 📉 Explained variance calculation
- 🎯 Principal component extraction
- 👥 Projection of individuals
- 📌 Projection of variables
- 🔄 Correlation Circle visualization
- 📊 Individual factor maps
- 📈 Biplot visualization
- ⭐ Cos² (Quality of Representation)
- 📌 Contribution of individuals
- 📌 Contribution of variables
- 📉 Distance to the centroid
- 📋 Complete statistical interpretation

---

# 📑 Project Report

## Project Objective

Principal Component Analysis (PCA) is one of the most widely used techniques in multivariate statistics for analyzing datasets containing many correlated variables.

The objective of this project is to implement the entire PCA pipeline without relying on dedicated PCA libraries.

The implementation allows the user to:

- Reduce dimensionality
- Visualize high-dimensional datasets
- Discover hidden relationships
- Identify the most influential variables
- Interpret principal components
- Analyze similarities between observations

The project demonstrates both the mathematical theory and practical implementation of PCA.

---

# 🧠 Why Principal Component Analysis?

Real-world datasets often contain many correlated variables that make visualization and interpretation difficult.

PCA transforms the original variables into a new orthogonal coordinate system where:

- Each principal component explains a portion of the total variance.
- Components are uncorrelated.
- The first few components capture most of the information.

Benefits include:

- Dimensionality reduction
- Noise reduction
- Data visualization
- Feature extraction
- Compression
- Better understanding of correlations

---

# 🔬 Mathematical Principle

Given a standardized data matrix:

\[
Z = \frac{X-\mu}{\sigma}
\]

the algorithm computes:

1. Correlation matrix

\[
R=\frac{1}{n}Z^TZ
\]

2. Eigenvalues

\[
R u_i=\lambda_i u_i
\]

3. Principal Components

\[
F=ZU
\]

where

- λ = explained variance
- U = eigenvectors
- F = factor coordinates

The percentage of inertia explained by each component is

\[
\frac{\lambda_i}{\sum \lambda_i}\times100
\]

---

# ⚙️ PCA Workflow

## 1️⃣ Data Loading

The dataset is loaded into a NumPy matrix.

Examples include:

- Cities × Sports dataset
- Beverage sensory dataset

---

## 2️⃣ Data Standardization

Each variable is centered and normalized:

- Mean = 0
- Variance = 1

This prevents variables with larger scales from dominating the analysis.

---

## 3️⃣ Correlation Matrix

The standardized data are used to compute the correlation matrix, which summarizes relationships among variables.

---

## 4️⃣ Eigen Decomposition

The correlation matrix is decomposed into:

- Eigenvalues
- Eigenvectors

Eigenvalues determine the importance of each principal component.

---

## 5️⃣ Principal Components

Individuals are projected into the new factor space.

This projection enables visualization in two or three dimensions while preserving as much variance as possible.

---

## 6️⃣ Analysis of Individuals

The project computes:

- Coordinates
- Distance from centroid
- Cos² quality of representation
- Contributions
- Poorly represented individuals

The factor maps reveal similarities and clusters among observations.

---

## 7️⃣ Analysis of Variables

The variables are analyzed using:

- Factor coordinates
- Correlations
- Cos²
- Contributions
- Correlation circles

The correlation circle helps identify:

- Strongly correlated variables
- Opposite variables
- Independent variables

---

## 8️⃣ Biplot

A complete biplot combines:

- Individuals
- Variables

inside the same principal component space.

This provides simultaneous interpretation of observations and variables.

---

# 📊 Evaluation Metrics

The project computes:

- Eigenvalues
- Explained Variance
- Cumulative Variance
- Coordinates of Individuals
- Coordinates of Variables
- Cos² of Individuals
- Cos² of Variables
- Contribution of Individuals
- Contribution of Variables
- Distances from the Centroid

---

# 🏗️ Pipeline

## 1️⃣ Load Dataset

- Import data
- Create data matrix

---

## 2️⃣ Standardize Data

- Center variables
- Normalize variance

---

## 3️⃣ Compute Correlation Matrix

- Pearson correlation matrix

---

## 4️⃣ Eigen Decomposition

- Eigenvalues
- Eigenvectors

---

## 5️⃣ Principal Components

- Projection of individuals
- Projection of variables

---

## 6️⃣ Visualizations

Generate:

- Scree Plot
- Individual Factor Map
- Correlation Circle
- Variable Factor Map
- Biplot

---

## 7️⃣ Interpretation

Study:

- Dominant variables
- Representative individuals
- Explained variance
- Correlations

---

# 📂 Project Structure

```text
Principal-Component-Analysis-PCA-From-Scratch/
│
├── TP3_ACP_Solution.ipynb
├── TP3_boissons.ipynb
├── TP 3 (IV)25-26.pdf
│
├── figures/
│   ├── scree_plot.png
│   ├── correlation_circle.png
│   ├── factor_map.png
│   ├── biplot.png
│   └── inertia.png
│
├── results/
│   ├── eigenvalues.csv
│   ├── contributions.csv
│   ├── cos2.csv
│   └── coordinates.csv
│
└── README.md
```

---

# ▶️ Running the Project

Install the required packages

```bash
pip install numpy pandas matplotlib notebook
```

Launch Jupyter Notebook

```bash
jupyter notebook TP3_ACP_Solution.ipynb
```

or

```bash
jupyter notebook TP3_boissons.ipynb
```

You may also execute the notebooks using **Google Colab**.

---

# 📈 Generated Visualizations

The notebooks generate several statistical visualizations:

- 📊 Scree Plot
- 👥 Individuals Projection
- 📈 Variables Projection
- 🔄 Correlation Circle
- 📉 Explained Variance Plot
- 📌 Contributions
- ⭐ Cos² Analysis
- 📊 Biplot

---

# ✅ Strengths

- PCA implemented from scratch
- No dedicated PCA library required
- Fully reproducible mathematics
- Rich statistical interpretation
- Correlation circle visualization
- Biplot visualization
- Individual and variable analysis
- Clean NumPy implementation
- Educational and research oriented

---

# ⚠️ Limitations

- PCA assumes linear relationships
- Sensitive to outliers
- Requires standardized variables
- Interpretation becomes harder with many dimensions
- Visualization limited to first principal components

---

# 🚀 Future Improvements

- Kernel PCA
- Sparse PCA
- Incremental PCA
- Interactive Plotly visualizations
- 3D PCA visualization
- Automatic interpretation reports
- Comparison with Scikit-Learn PCA
- Export results to PDF

---

# 🛠️ Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook
- Linear Algebra
- Eigenvalue Decomposition

---

# 📚 References

- Karl Pearson (1901) — On Lines and Planes of Closest Fit to Systems of Points in Space
- Hotelling, H. (1933) — Analysis of a Complex of Statistical Variables
- Jolliffe, I. T. — Principal Component Analysis
- NumPy Documentation
- Pandas Documentation
- Matplotlib Documentation
- USTHB — Master MIV — Data Analysis Laboratory
