# 📊 Exploratory Data Analysis (EDA) – Stores Dataset  

## 📌 Project Overview  
This repository contains the **Exploratory Data Analysis (EDA)** performed on the **Stores dataset**.  
The goal was to explore, clean, visualize, and derive insights from store-related attributes such as area, items available, daily customer count, and sales.  

---

## 📂 Dataset Details  
- **File:** `Stores.csv`  
- **Rows:** 896  
- **Columns:** 5  
  - `Store ID`  
  - `Store_Area`  
  - `Items_Available`  
  - `Daily_Customer_Count`  
  - `Store_Sales`  

---

## ⚙️ Basic EDA Performed  
1. Loaded dataset and inspected shape, datatypes, and column details  
2. Checked for missing values → none found  
3. Generated descriptive statistics (mean, median, std, min, max, percentiles)  
4. Checked skewness and distribution of numeric features  
5. Identified and treated outliers (IQR method with capping)  
6. Created new derived features (`Sales_per_Customer`, `Items_Density`, `Log_Sales`, `Customer_Bin`)  
7. Exported the cleaned dataset as `Stores_Cleaned.csv`  

---

## 📊 Graphs & Visualizations (Elaborated Summary)

### 🔹 Univariate Analysis
1. **Histograms** – Showed the distribution of each numerical feature (`Store_Area`, `Items_Available`, `Daily_Customer_Count`, `Store_Sales`). Helped to understand data spread and skewness.  
2. **Boxplots** – Used to detect outliers in numeric columns. Revealed extreme values in `Store_Sales` and `Daily_Customer_Count`.  
3. **KDE Plots** – Displayed smoothed probability distributions. Showed that `Items_Available` is nearly normal while `Store_Sales` is right-skewed.  
4. **ECDF Plot** – Cumulative distribution for `Store_Sales`. Showed that ~80% of stores make below a certain sales level, highlighting inequality.  

### 🔹 Bivariate Analysis
5. **Scatterplot (Store_Area vs Store_Sales)** – Larger stores generally report higher sales, but a few outliers exist.  
6. **Scatterplot (Items_Available vs Store_Sales)** – Weak positive relation, showing items stocked do not strongly drive sales.  
7. **Scatterplot (Daily_Customer_Count vs Store_Sales)** – Strong positive correlation, confirming customers are the key driver of sales.  
8. **Regression Plot (Store_Area vs Store_Sales)** – Confirmed linear upward trend between store area and sales.  
9. **Hexbin Plot (Customer_Count vs Store_Sales)** – Showed dense clusters where medium-sized stores with average customers dominate.  

### 🔹 Multivariate Analysis
10. **Correlation Heatmap** – Strongest correlation found between `Daily_Customer_Count` and `Store_Sales`.  
11. **Pairplot** – Gave a combined view of relationships among all numerical features.  
12. **Violin Plots** – Showed distribution + spread of variables, highlighting concentration of values.  
13. **Swarm Plot** – Displayed distribution of sales with respect to store area in a detailed manner.  
14. **Strip Plot** – Spread of customer counts against store sales, revealing clusters.  
15. **Density Contour Plot (2D KDE)** – Showed joint distribution of `Customer_Count` and `Store_Sales`, confirming strong dependency.  

### 🔹 Advanced Plots
16. **Bar Plot (Customer_Bin vs Avg Sales)** – Higher customer bins correspond to higher average sales.  
17. **Count Plot (Customer_Bin)** – Distribution of stores across different customer count bins.  
18. **Line Plot (Store_Area vs Store_Sales)** – Trend line confirmed that larger stores drive higher sales.  
19. **Hexbin Plot (Items_Available vs Store_Sales)** – Highlighted store clusters with mid-range items and average sales.  
20. **Distribution Plot (Log_Sales)** – After log transformation, sales distribution became more normalized.  

---

## 📈 Tools & Libraries Used  
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scipy  

---

## 👤 Author  
**Hrithik Kumar**  
_Data Analyst_  
