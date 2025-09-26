# 🛡️ Insurance Cost Analysis & Prediction  

Unlocking the hidden patterns behind **medical insurance costs** 💰 using data analysis and statistics!  
This project dives deep into a health insurance dataset to understand how **age, BMI, smoking habits, and lifestyle choices** affect medical expenses.  

---

## 🚀 Project Highlights  

### 🔍 Exploratory Data Analysis (EDA)  
- 📂 Loaded **1338 records** with 7 key features.  
- ✅ No missing values detected.  
- 📊 Visualized distributions (histograms, KDEs) for age, BMI, children, and charges.  
- 🔥 Correlation heatmap revealed **smoking** as the strongest predictor of charges (~0.79).  

### 🧹 Data Cleaning & Preprocessing  
- 🗑️ Removed duplicates (final dataset = **1337 rows**).  
- 🔄 Converted categories to numbers:  
  - `sex → is_female (0/1)`  
  - `smoker → is_smoker (0/1)`  
- 🏷️ Added **BMI Category** (Underweight, Normal, Overweight, Obese).  
- 🌍 One-hot encoded `region`.  
- 📏 Standardized numerical features (`age`, `bmi`, `children`).  

### 📊 Statistical Analysis  
- 📈 Pearson correlation:  
  - Smoking 🚬 → **highest positive impact** on charges.  
  - Age & BMI also moderately correlated.  
- 🧮 Chi-Square tests:  
  - Confirmed **smoking, obesity, gender, and southeast region** are significant predictors (p < 0.05).  

### 🎨 Visualizations  
- 📊 Histograms & KDEs → Distribution insights.  
- 📦 Boxplots → Outlier detection.  
- 🌡️ Heatmaps → Relationships between features.  
- 🧾 Value counts → Gender, smoker ratio, regional spread.  

---

## 💻 Tech Stack  

- 🐍 **Python 3.x**  
- 📦 **Pandas, NumPy** – data wrangling  
- 🎨 **Matplotlib, Seaborn** – plots & visualizations  
- ⚙️ **Scikit-learn** – preprocessing (StandardScaler, encoding)  
- 🔬 **SciPy** – correlations & Chi-Square tests  
- 📓 **Jupyter Notebook** – interactive analysis  

---

## 📊 Dataset Overview  

The dataset (1338 entries, commonly from **Kaggle/UCI**) includes:  

| Feature     | Description |
|-------------|-------------|
| age         | Age of insured (years) |
| sex / is_female | Gender (female=1, male=0) |
| bmi         | Body Mass Index (kg/m²) |
| children    | Number of dependents |
| smoker / is_smoker | Smoking status (yes=1, no=0) |
| region      | Residential area (northeast, southeast, etc.) |
| charges     | Annual medical costs (USD) |

---
 

