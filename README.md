# Task 1 — Retail Sales: Exploratory Data Analysis

**Oasis Infobyte Internship Program (OIBSIP) — Data Analytics Track**
**Author:** Karan Verma

## Objective

Explore a retail transactions dataset to understand how revenue is distributed
across product categories, customer demographics, and time — and surface
insights that could realistically inform business decisions like stocking,
staffing, or promotional timing.

## Dataset

`retail_sales_dataset.csv` — 1,000 retail transactions with the following columns:

| Column | Description |
|---|---|
| Transaction ID | Unique ID per transaction |
| Date | Date of transaction (2023) |
| Customer ID | Unique customer identifier |
| Gender | Male / Female |
| Age | Customer age (18–64) |
| Product Category | Beauty, Clothing, or Electronics |
| Quantity | Units purchased |
| Price per Unit | Price per unit (₹) |
| Total Amount | Quantity × Price per Unit |

The dataset had no missing values and no duplicate rows, so cleaning was minimal —
mainly converting `Date` to a proper datetime type to enable time-based analysis.

## Tools Used

Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook.

## Approach

1. Loaded and inspected the data (shape, types, missing values, duplicates).
2. Engineered extra fields: `Month`, `Weekday`, `AgeGroup`.
3. Univariate analysis — distributions of age, gender, category, and transaction value.
4. Bivariate analysis — revenue by category, gender, age group, weekday, and month;
   correlation between Age, Quantity, Price per Unit, and Total Amount.

Full step-by-step code, charts, and explanations are in
[`Karan_Verma_Task1.ipynb`](./Karan_Verma_Task1.ipynb).

## Key Insights

**1. Revenue is fairly balanced across categories.** Electronics narrowly leads
(₹1,56,905), just ahead of Clothing (₹1,55,580) and Beauty (₹1,43,515) — under a
9% gap between the highest and lowest category.

![Revenue by category](./charts/revenue_by_category.png)

**2. Price per unit drives revenue far more than quantity or age.** Total Amount
correlates strongly with Price per Unit (0.85), moderately with Quantity (0.37),
and barely at all with Age (-0.06).

![Correlation heatmap](./charts/correlation_heatmap.png)

**3. Spending habits shift by age group, but not by product preference.** The
45–54 age group generates the most total revenue (₹1,00,690) simply by
transacting more often, while 18–24 year-olds spend the most per visit on
average (₹500) — younger customers buy less often but spend more each time.

**4. Saturday is the strongest sales day** (₹78,815) and **Thursday the
weakest** (₹53,835), suggesting a weekend shopping pattern.

![Revenue by weekday](./charts/revenue_by_weekday.png)

**5. No clean seasonal trend across the year** — monthly revenue swings between
₹23,620 (September) and ₹53,150 (May) without a steady seasonal pattern,
suggesting revenue at this scale is driven by individual high-value
transactions rather than a calendar effect.

![Monthly revenue trend](./charts/monthly_revenue_trend.png)

## Conclusion

This dataset shows a retail business with broadly balanced demand across
categories and genders, where **the price point of what's being sold matters
far more than who buys it or how much they buy in one go**. The clearest
actionable patterns are the Saturday sales peak and the higher per-visit spend
among 18–24 year-olds — both useful angles for promotional timing and
targeted marketing.

## How to Run

```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook Karan_Verma_Task1.ipynb
```

(Or upload the notebook and CSV to Google Colab and run all cells.)

## Repository Structure

```
Karan_Verma_Task1/
├── Karan_Verma_Task1.ipynb     # Full analysis notebook
├── retail_sales_dataset.csv    # Dataset
├── README.md                   # This file
└── charts/                     # Exported chart images used in this README
```
