# Retail Customer Sales: Exploratory Data Analysis

**Author:** Bhavesh Bansal | **Roll No:** 2026M01410046
**Program:** Data Analyst Training Program | **Project 1:** Understanding, Cleaning & Profiling Retail Customer Sales Data

A complete exploratory data analysis (EDA) of two years (2023-2024) of retail customer sales across four regions of India. The project audits the raw data, cleans it with documented and conservative decisions, profiles it, and turns the results into business takeaways.

**Headline result:** 7,084 raw records were audited and cleaned into **7,000 verified transactions** representing **₹7.67 Crore in sales** and **₹2.51 Crore in profit** (32.7% average margin).

---

## Project Objectives

1. **Setup & First Look:** load the dataset and understand its structure
2. **Data Quality Audit:** find missing values, duplicates, inconsistencies and impossible values
3. **Data Cleaning:** apply and justify every cleaning decision
4. **Data Profiling:** explore distributions, trends and relationships
5. **Business Insights:** answer key business questions with evidence

---

## Dataset

| Item | Details |
|------|---------|
| File | `retail_customer_sales_dataset.csv` |
| Raw size | 7,084 records, 24 columns |
| Cleaned size | 7,000 records (`cleaned_retail_customer_sales.csv`) |
| Period | 2023 - 2024 |
| Coverage | 4 regions of India (North, South, East, West) |
| Categories | Electronics, Furniture, Clothing, Grocery, Office Supplies |

---

## Data Quality Audit and Cleaning

| Issue Found | How Often | How It Was Handled |
|-------------|-----------|--------------------|
| Duplicate orders | 84 (61 exact copies + 23 hidden behind spelling/date differences) | Removed after standardizing labels and dates, so revenue is not double-counted |
| Inconsistent spelling and casing | Gender written 8 ways; Region written 12 ways (e.g. `Nort`, `Sth`) | Unified to Male/Female and North/South/East/West |
| Mixed date formats and impossible timelines | 4 date styles; 15 orders delivered before they were placed | Standardized to one format; cleared the 15 impossible delivery dates |
| Impossible ages and discounts | 6 ages (<18 or >100, e.g. -12, 999); 6 discounts (<0% or >100%) | Replaced with the median instead of deleting valid sales rows |
| Missing values | Income 253, Age 142, Discount 71, Rating 428, Satisfaction 179 | Median fill for Income, Age and Discount; Satisfaction labeled `Unknown`; unrated orders left blank |

---

## Key Findings

1. **Typical baskets are small; big-ticket orders lift the average.** The median order is **₹4,826** versus a mean of **₹10,962**. Electronics and Furniture orders (up to ₹1,22,951) pull the average up.
2. **Electronics and Furniture generate 83% of revenue.** Electronics (₹3.76 Cr) and Furniture (₹2.61 Cr) dominate, while Grocery and Clothing account for nearly half of all orders and drive store traffic.
3. **Customers are working-age adults.** Median age is **36** (middle half: 29-43). Median income is about **₹49,005**, with a small affluent group earning up to ₹17.51 lakh.
4. **Margins are steady at 32%-33%.** Profit margin stays between 32.3% and 33.0% across all categories and regions, with discounts averaging 18%-20%.
5. **Regional sales are well balanced.** East (₹2.00 Cr) and West (₹1.98 Cr) lead, followed by South (₹1.89 Cr) and North (₹1.81 Cr). East has the largest average order (₹11,342).
6. **Shipping tiers look identical in practice.** Delivery takes 5.6-5.8 days and return rates are 12.4%-12.8% for Standard, Express and Same-Day alike. Customer segments and payment methods are also evenly spread.

### Category Snapshot

| Category | Orders | Median Order | Mean Order | Total Revenue | Total Profit | Avg Margin |
|----------|--------|--------------|------------|---------------|--------------|------------|
| Electronics | 1,975 (28.2%) | ₹15,451 | ₹19,058 | ₹3,76,39,557 | ₹1,23,52,220 | 32.9% |
| Furniture | 979 (14.0%) | ₹21,490 | ₹26,617 | ₹2,60,57,894 | ₹85,47,605 | 32.9% |
| Clothing | 1,533 (21.9%) | ₹4,199 | ₹5,076 | ₹77,81,680 | ₹25,21,028 | 32.3% |
| Grocery | 1,669 (23.8%) | ₹1,324 | ₹1,609 | ₹26,85,875 | ₹8,74,840 | 32.4% |
| Office Supplies | 844 (12.1%) | ₹2,445 | ₹3,041 | ₹25,66,183 | ₹8,32,190 | 32.8% |
| **All Orders** | **7,000** | **₹4,826** | **₹10,962** | **₹7,67,31,189** | **₹2,51,27,883** | **32.7%** |

---

## Recommendations

- **Audit Express and Same-Day fulfillment:** these orders average nearly 6 days, so customers paying for speed may not be getting it.
- **Bundle high-frequency and high-margin items:** use Grocery and Clothing checkouts to promote Electronics and Furniture accessories.
- **Add input validation at data entry:** use dropdowns for Region and Gender, block out-of-range ages and discounts, and prevent delivery dates earlier than order dates.



---

## Repository Structure

```
retail_sales_EDA/
├── BhaveshBansal_2026M01410046_EDA_Project.ipynb   # Main analysis notebook
├── retail_customer_sales_dataset.csv               # Raw dataset
├── cleaned_retail_customer_sales.csv               # Cleaned dataset
├── Output/                                         # Charts (1.png - 8.png)
├── Reports/
│   ├── BhaveshBansal_2026M01410046_EDA_Insights_Report.pdf
│   ├── BhaveshBansal_2026M01410046_EDA_SRS.pdf
│   └── BhaveshBansal_EDA_Project_Synopsis.pdf
└── README.md
```

---

## Tools and Libraries

Python 3.11, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook (VS Code), Git and GitHub

---

## How to Run

```bash
git clone https://github.com/Bhaveshtech20/retail_sales_EDA.git
cd retail_sales_EDA
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook BhaveshBansal_2026M01410046_EDA_Project.ipynb
```

Run all cells from top to bottom. Charts are saved to `Output/`.

---

## Contact

**Bhavesh Bansal** | GitHub: [@Bhaveshtech20](https://github.com/Bhaveshtech20)