# Amazon Sales — Revenue & Customer Behavior Analysis

> Exploratory data analysis and customer segmentation on ~50,000 e-commerce orders across 6 product categories and 4 global regions (2022–2023).

---

## Business problem

An e-commerce platform needs to understand:
- Which product categories drive the most revenue
- How discounts affect profitability
- Where seasonality peaks occur
- What customer and product segments exist to guide marketing decisions

---

## Key findings

| # | Finding | Impact |
|---|---------|--------|
| 1 | **Discounts above 20% reduce avg order revenue by ~18%** ($749 → $614) without volume compensation | Cap discounts at 15% to protect margins |
| 2 | **January post-holiday spike is consistent** across both years, followed by a ~13% February dip | Optimize inventory and ad spend before January |
| 3 | **Revenue is balanced across all 6 categories** (max gap: $143K out of $32.8M total) | No single-category dependency risk |
| 4 | **3 product segments identified** via K-Means: High Performance, High Price–Low Volume, Low Price–High Volume | Each segment requires a different pricing strategy |
| 5 | **Discount-driven customers rate products lower** than non-discount buyers | Heavy discounts may attract lower-quality demand |

---

## Analysis outline

```
1. Setup & data loading
2. Data quality check          — nulls, dtypes, duplicates
3. Descriptive statistics      — df.describe(), value counts
4. Business queries (10)       — revenue, trends, regions, payments, ratings, discounts
5. Correlation analysis        — numeric variable relationships
6. K-Means clustering #1       — product behavior segments
7. K-Means clustering #2       — customer satisfaction segments
8. Key findings summary
```

---

## Charts

| Query | Question answered |
|-------|------------------|
| Revenue by category | Which categories generate the most revenue? |
| Monthly revenue trend | Is there seasonality? |
| Units sold by region | Which regions have the highest volume? |
| Payment methods | What are customer payment preferences? |
| Avg rating by category | Which categories have the highest satisfaction? |
| Discount vs revenue | Do higher discounts hurt profitability? |
| Reviews by category | Which categories drive the most engagement? |
| Revenue by region × category | Which combinations yield the highest order value? |
| Avg price by category | Are products consistently priced? |
| Monthly units trend | Does volume mirror revenue seasonality? |

---

## Stack

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.x-F7931E?logo=scikit-learn)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.x-blue)
![Seaborn](https://img.shields.io/badge/Seaborn-0.13-blue)
![KNIME](https://img.shields.io/badge/KNIME-5.x-yellow)

---

## How to run

```bash
# 1. Clone the repo
git clone https://github.com/your-username/amazon-sales-analysis.git
cd amazon-sales-analysis

# 2. Install dependencies
pip install pandas matplotlib seaborn scikit-learn notebook

# 3. Download the dataset from Kaggle and place it in /data
#    https://www.kaggle.com/datasets/aliiihussain/amazon-sales-dataset

# 4. Launch the notebook
jupyter notebook notebooks/amazon_sales_eda.ipynb
```

---

## Dataset

**Amazon Sales Dataset** by Ali Hussain — available on [Kaggle](https://www.kaggle.com/datasets/aliiihussain/amazon-sales-dataset)

- ~50,000 orders
- 13 variables: order date, product category, price, discount, quantity sold, region, payment method, rating, review count, revenue
- Date range: January 2022 – December 2023
- 4 regions: Asia, Europe, Middle East, North America
- 6 categories: Beauty, Books, Electronics, Fashion, Home & Kitchen, Sports

> The dataset is not included in this repository. Download it directly from Kaggle using the link above.

---

## Project structure

```
amazon-sales-analysis/
├── notebooks/
│   └── amazon_sales_eda.ipynb
├── data/
│   └── README.md              ← download instructions
├── images/                    ← exported charts
└── README.md
```
