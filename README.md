# 🛡️ Insurance Cost Analysis & Prediction

This project analyzes a medical insurance dataset to explore factors affecting **insurance charges**.  
The Jupyter Notebook performs comprehensive data analysis and preprocessing steps, including **Exploratory Data Analysis (EDA)**, **feature engineering**, and **statistical analysis**.  
The goal is to understand how demographics (age, sex, BMI, etc.) and lifestyle factors (smoking, region) influence insurance costs, providing a foundation for future predictive modeling.

---

## 🚀 Features & Workflow

### 🔍 Exploratory Data Analysis (EDA)
- Loaded the insurance CSV dataset (**1338 records, 7 columns**).  
- Inspected data types and summary (`age`, `sex`, `bmi`, `children`, `smoker`, `region`, `charges`).  
- Checked for missing values – **no nulls found**.  
- Plotted distributions (histograms and KDEs) for numeric features and boxplots for outliers.  
- Generated a **correlation heatmap** to visualize relationships between numeric variables.  

### 🧹 Data Cleaning & Preprocessing
- Removed duplicate entries (final rows = **1337**).  
- Converted categorical variables to numeric:  
  - `sex` → `is_female` (0/1)  
  - `smoker` → `is_smoker` (0/1)  
- Created a new feature **BMI Category** using `pd.cut` (Underweight, Normal, Overweight, Obese) and one-hot encoded it.  
- One-hot encoded the **region** feature (drop-first to avoid multicollinearity).  
- Standardized numerical columns (`age`, `bmi`, `children`) using **StandardScaler**.  

### 📊 Statistical Analysis & Feature Selection
- Calculated **Pearson correlation** with charges:  
  - `is_smoker` → ~0.79 (highest positive correlation)  
  - `age` → ~0.30  
  - `bmi` → ~0.20  
- Performed **Chi-Square tests** on categorical features:  
  - Significant predictors: **smoking, region (southeast), gender, obesity** (p < 0.05)  
  - Insignificant predictors: some regions, non-obese BMI categories.  

### 🎨 Visualization
- **Histograms & KDEs** → age, BMI, children, charges.  
- **Boxplots** → outlier detection.  
- **Heatmap** → correlations among numeric features.  
- **Value Counts** → smokers vs non-smokers, regional distribution.  

---

## 💻 Technologies & Libraries
- **Language:** Python 3.x  
- **Data Handling:** pandas, numpy  
- **Visualization:** matplotlib, seaborn  
- **Preprocessing:** scikit-learn (StandardScaler), pandas (get_dummies)  
- **Statistical Tests:** SciPy (Pearson correlation, Chi-Square)  
- **Notebook:** Jupyter Notebook  

📚 *All code is in the `Insurance.ipynb` notebook.*

---

## 📊 Dataset
The dataset (often found on **Kaggle** or **UCI**) contains **1338 medical insurance records**.  

| Feature          | Description                                |
|------------------|--------------------------------------------|
| `age`            | Age of primary beneficiary (years)         |
| `sex` / `is_female` | Gender (female=1, male=0)              |
| `bmi`            | Body Mass Index (kg/m²)                    |
| `children`       | Number of dependent children               |
| `smoker` / `is_smoker` | Smoking status (yes=1, no=0)        |
| `region`         | Residential region (northeast, etc.)       |
| `charges`        | Medical insurance charges (dollars)        |
