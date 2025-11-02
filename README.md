#  Feature Engineering on Electric Production Dataset

## Project Overview
This project demonstrates **feature engineering and preprocessing** techniques on the **Electric_Production.csv** dataset.  
The goal is to clean, transform, and prepare the dataset for machine learning applications by applying various data preprocessing, encoding, scaling, and dimensionality reduction techniques.

---

##  Dataset Description
**Dataset:** Electric_Production.csv  
**Source:** Kaggle – Time Series Datasets (Electric Production Data)  
**Description:**  
The dataset contains monthly records of **total electric power production in the United States** from **January 1985 to May 2018**.  
It includes the following features:
- `IPG2211A2N`: Electric power production value  
- `Year`: Year of record  
- `Month`: Month of record  
- `Quarter`: Quarter of the year  

---

##  Steps Performed

### 1️⃣ Data Loading and Exploration
- Loaded the dataset using **pandas**.
- Checked for **missing values**, **data types**, and **basic statistics**.

### 2️⃣ Missing Data Handling
- Missing numeric values were handled using **mean imputation** with `SimpleImputer`.

### 3️⃣ Feature Engineering
- Created a **DATE** column by combining `Year` and `Month` for time-based analysis.
- Converted categorical column `Quarter` into dummy variables using **One-Hot Encoding**.

### 4️⃣ Feature Scaling
- Applied **StandardScaler** to standardize the numeric features so that they have a mean of 0 and standard deviation of 1.

### 5️⃣ Dimensionality Reduction
- Implemented **Principal Component Analysis (PCA)** to reduce dimensionality and capture the most important variance in the data.

### 6️⃣ Feature Selection
- Used **SelectKBest** with `f_regression` to identify the most significant features for predictive modeling.

---

## 🧩 Summary of Transformations
| Step | Purpose | Outcome |
|------|----------|----------|
| Missing Value Handling | Replace NaN with mean | Dataset becomes complete |
| Encoding | Convert categorical data | Model interprets categorical info |
| Scaling | Normalize numeric range | Ensures balanced feature influence |
| PCA | Reduce dimensionality | Extracts key patterns |
| Feature Selection | Pick important features | Improves model efficiency |

---

## 💡 Observations
- The dataset is now **clean and standardized**.  
- PCA revealed that **one principal component** captures most of the variance.  
- Encoded features improved model interpretability.  
- The new `DATE` column provides useful temporal structure.

---

## ⚖️ Ethical Considerations
Although this dataset is not sensitive, in other projects (like employee attrition or loan prediction), using personal attributes such as **Gender** or **Marital Status** may cause **bias** or **discrimination**.  
To mitigate bias:
- Remove sensitive columns from training.
- Apply **fairness-aware algorithms**.
- Regularly monitor model outcomes using **fairness metrics**.

---

## 🧰 Technologies Used
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib / Seaborn (optional for visualization)  
- Jupyter Notebook / Google Colab  

---

## 📁 Repository Structure
```
├── Electric_Production.csv
├── Feature_Engineering_Electric_Production.ipynb
├── Feature_Engineering.docx
├── README.md
```

---

## 🚀 How to Run
1. Clone this repository  
   ```bash
   git clone https://github.com/piyush-ouch/feature-engineering.git
   ```
2. Open the notebook:
   ```bash
   jupyter notebook Feature_Engineering_Electric_Production.ipynb
   ```
3. Run all cells to reproduce results.

---

## ✍️ Author
**Piyush Jangade**  
B.Tech in Artificial Intelligence and Machine Learning, MITAOE  
