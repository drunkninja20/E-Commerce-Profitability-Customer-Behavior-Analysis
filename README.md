# 🛒 E-Commerce Profitability & Customer Behavior Analysis

Analyze sales, profit, and customer behavior from the [Superstore](https://www.kaggle.com/datasets/rohithmandalapu/superstore-dataset-final) dataset using pandas, numpy, matplotlib, and seaborn.

---

## 📦 Project Overview

This project delivers actionable insights into trends in sales, profit, customer segments, regions, and products for an e-commerce retailer. The approach is hands-on and data-driven, with a focus on:

- Cleaning and preprocessing raw sales data
- Exploring seasonal, regional, and segment-level profitability
- Detecting products and locations driving losses
- Calculating Year-over-Year (YoY) growth in sales and profit
- Providing business-ready recommendations

---

## 🧑‍💻 Technologies Used

- **Python 3**
- **pandas** for data wrangling and analysis
- **numpy** for numerical computations
- **matplotlib/seaborn** for visualizations

---

## 📁 Dataset

- **File:** `superstore.csv`
- **Columns:** `Order Date`, `Ship Date`, `Category`, `Sub-Category`, `Sales`, `Profit`, `Quantity`, `Discount`, `Region`, etc.
- **Rows:** ~10,000
- **Source:** [Kaggle Superstore Dataset](https://www.kaggle.com/datasets/rohithmandalapu/superstore-dataset-final)

---

## 🚦 Quick Start

Clone the repository and install dependencies:

git clone https://github.com/yourusername/ecommerce-profitability-analysis.git
cd ecommerce-profitability-analysis
pip install pandas numpy matplotlib seaborn

Run the analysis:

- Open and run the notebook: `E-Commerce-Profitability-Customer-Behavior-Analysis.ipynb`

---

## 📝 Example: Calculating Year-over-Year (YoY) Growth
import pandas as pd

df = pd.read_csv("superstore.csv", encoding='windows-1252')
df['Order Date'] = pd.to_datetime(df['Order Date'])
df['Year'] = df['Order Date'].dt.year

sales_per_year = df.groupby('Year')['Sales'].sum().sort_index()
sales_per_year = sales_per_year.to_frame()
sales_per_year['YoY Growth (%)'] = sales_per_year['Sales'].pct_change() * 100

---

## 🔍 Key Analysis Performed

- **Data Cleaning:** Fix column names, handle missing values, convert date types
- **Descriptive Analysis:** `.describe()`, `.groupby()`, `.agg()` for rapid KPI checks
- **Profit/Loss Deep Dives:** Analyze negative profit margins across categories and sub-categories
- **Segmentation:** Revenue breakdown by region, segment, category, and product
- **Trend Analysis:** Time-based sales/profit patterns, Year-over-Year (YoY) growth
- **Visualization:** Bar plots, line charts, heatmaps for insight communication

---

## 📈 Example Insights

- 📉 *Identified sub-categories ("Tables", "Bookcases", "Machines") that consistently generate losses*
- 🌎 *Found regional trends; e.g., "West" region outperforms, "South" lags in profit*
- 📅 *YoY sales and profit growth tracked; clear impact of seasonality visible*
- 🎯 *Recommended discounts targeted only at price-sensitive products to prevent margin loss*


## 🤝 Contributing

Contributions and suggestions are welcome. Open an issue to discuss your ideas or submit a pull request.

---

## 📚 Reference

- [pandas Documentation](https://pandas.pydata.org/docs/)
- [Superstore Dataset on Kaggle](https://www.kaggle.com/datasets/rohithmandalapu/superstore-dataset-final)

---

**Happy analyzing!**

