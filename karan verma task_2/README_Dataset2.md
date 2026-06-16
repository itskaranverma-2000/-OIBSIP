# Task 1 — Dataset 2: McDonald's Menu Nutrition Analysis

**Name:** Karan Verma  
**Internship:** Oasis Infobyte (OIBSIP)  
**Domain:** Data Analytics  

---

## Problem Statement
Analyze McDonald's menu nutrition data to find patterns in calories, fat, protein, and other nutrients across different menu categories.

## Dataset
- **Source:** Kaggle — Nutrition Facts for McDonald's Menu
- **Records:** 260 menu items
- **Features:** 24 columns (Category, Item, Calories, Fat, Protein, Sodium, Sugar, etc.)
- **Missing Values:** None

## Tools Used
- Python, Pandas, Matplotlib, Seaborn, NumPy, Google Colab

## Key Findings
1. **Chicken & Fish** items have highest average calories (553 cal) — Beverages lowest (114 cal)
2. **Chicken McNuggets (40 piece)** is the most calorie-dense item at 1880 calories
3. **Total Fat** has the strongest correlation with Calories (0.90) — fat is the biggest calorie driver
4. **Protein** also strongly correlates with calories (0.79) — higher protein = higher calories
5. **Smoothies & Shakes** and **Breakfast** items are surprisingly high in calories (531 & 527 avg)

## Recommendations
- Customers watching calories should choose Beverages, Desserts, or Salads
- Chicken & Fish category needs portion-size awareness — highest calorie category
- Smoothies marketed as "healthy" are actually calorie-dense — consumer awareness needed

## Charts
- `mcd_calories_by_category.png` — Average calories per category
- `mcd_top10_calories.png` — Top 10 highest calorie items
- `mcd_correlation_heatmap.png` — Nutrition correlation heatmap
- `mcd_protein_vs_calories.png` — Protein vs Calories scatter plot

## How to Run
1. Upload `menu.csv` and `Karan_Verma_Task1_Dataset2.ipynb` to Google Colab
2. Run all cells with Shift+Enter
