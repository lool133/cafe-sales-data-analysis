# ☕ Cafe Sales Data Analysis

A complete data analysis project on a real-world café sales dataset, including:

- Data Cleaning & Preprocessing
- Exploratory Data Analysis (EDA)
- Outlier Detection & Handling
- Principal Component Analysis (PCA)
- Data Visualization
- Exporting Cleaned Data & PCA Results

---

## 📌 Project Overview

This project demonstrates an end-to-end data analysis workflow using Python and popular data science libraries.

The dataset contains café sales transactions with intentionally dirty data (missing values, invalid entries, duplicates, and outliers). The notebook cleans the data, explores patterns, reduces dimensionality using PCA, and generates visual insights.

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn

---

## 📂 Project Structure

```text
├── data_analysis.ipynb
├── dirty_cafe_sales.csv
├── cleaned_cafe_sales.csv
├── pca_cafe_sales.csv
├── fig1_distributions.png
├── fig2_categories.png
├── fig3_correlation.png
├── fig4_pca.png
└── README.md
```

---

## 🔍 Analysis Workflow

### 1. Data Loading

- Load the café sales dataset.
- Inspect dataset shape, columns, and missing values.

### 2. Data Cleaning

#### Invalid Values
Replace invalid entries such as:

```python
ERROR
UNKNOWN
```

with missing values (`NaN`).

#### Data Type Conversion

Convert:

- Transaction Date → Datetime
- Quantity → Numeric
- Price Per Unit → Numeric
- Total Spent → Numeric

#### Duplicate Removal

Remove duplicate records and reset indexing.

#### Missing Value Handling

- Numeric columns → Filled using median values.
- Categorical columns → Filled using mode values.

#### Outlier Treatment

Use the **Interquartile Range (IQR)** method to identify and cap outliers.

---

### 3. Principal Component Analysis (PCA)

#### Feature Scaling

The following features are standardized:

- Quantity
- Price Per Unit
- Total Spent

using:

```python
StandardScaler()
```

#### Dimensionality Reduction

PCA is applied to reduce the dataset into:

```python
n_components = 2
```

Resulting components:

- PC1
- PC2

---

### 4. Data Visualization

The project generates four visual reports:

#### 📊 Figure 1 – Sales Distribution

Shows distributions for:

- Total Spent
- Quantity
- Price Per Unit

#### 📈 Figure 2 – Sales by Category

Visualizes:

- Sales by Item
- Sales by Payment Method

#### 🔥 Figure 3 – Correlation Matrix

Heatmap showing correlations between numerical features.

#### 🧠 Figure 4 – PCA Analysis

Includes:

- Scree Plot
- PCA Scatter Plot

---

## 📤 Outputs

The notebook exports:

### Cleaned Dataset

```text
cleaned_cafe_sales.csv
```

### PCA Dataset

```text
pca_cafe_sales.csv
```

containing:

```text
PC1
PC2
Location
Payment Method
Item
```

---

## ▶️ How to Run

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Run the Notebook

```bash
jupyter notebook data_analysis.ipynb
```

or

```bash
jupyter lab
```

---

## 📊 Key Skills Demonstrated

- Data Cleaning
- Data Wrangling
- Feature Engineering
- Exploratory Data Analysis
- Statistical Analysis
- PCA
- Data Visualization
- Data Export & Reporting

---

## 👨‍💻 Author

Developed as a Data Analysis project demonstrating practical data preprocessing, visualization, and dimensionality reduction techniques using Python.
