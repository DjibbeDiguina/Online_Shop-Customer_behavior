#  Customer Behavior Analysis  
### Retail Revenue Intelligence & Customer Segmentation

<p align="left">

![Python](https://img.shields.io/badge/Python-Data%20Cleaning-blue)
![MySQL](https://img.shields.io/badge/MySQL-Business%20Analysis-orange)
![Power%20BI](https://img.shields.io/badge/PowerBI-Dashboard-yellow)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![Role](https://img.shields.io/badge/Target%20Role-Junior%20Data%20Analyst-blueviolet)

</p>

---

##  Table of Contents

- [Project Background](#project-background)
- [Strategic Focus Areas](#strategic-focus-areas)
- [Data Structure & Initial Checks](#data-structure--initial-checks)
- [Executive Summary](#executive-summary)
- [Insights Deep Dive](#insights-deep-dive)
- [Strategic Recommendations](#strategic-recommendations)
- [Assumptions & Caveats](#assumptions--caveats)
- [Repository Structure](#repository-structure)

---

# Project Background

As a Data Analyst embedded within a mid-sized retail organization, I was tasked with evaluating transactional purchase behavior to identify revenue concentration risks, customer loyalty dynamics, and pricing sensitivity patterns.

The company operates in the consumer retail sector, generating revenue through direct product sales across four primary categories:

- Clothing  
- Accessories  
- Footwear  
- Outerwear  

An optional subscription program exists to support retention and recurring engagement.

The dataset consists of:

- **3,900 transactions**
- **18 structured business variables**
- Customer demographics, product details, discounts, subscription status, and ratings

The objective of this analysis was to translate transactional data into actionable business intelligence supporting marketing, pricing, and retention strategy.

---

# Strategic Focus Areas

Insights and recommendations are structured around four business pillars:

1. **Revenue & Product Performance**
2. **Customer Segmentation & Loyalty**
3. **Discount Sensitivity & Pricing Behavior**
4. **Subscription Impact & Revenue Distribution**

SQL queries used for inspection and cleaning:  
👉 [Data Cleaning SQL](./sql/data_cleaning.sql)

Targeted SQL queries addressing business questions:  
👉 [Business Analysis SQL](./sql/business_queries.sql)

Interactive Power BI dashboard:  
👉 [Dashboard Link](#)

---

# Data Structure & Initial Checks

The core transactional dataset contains **3,900 records**.

For analytical clarity, the database structure was logically segmented into:

### Customers
- customer_id  
- age  
- gender  
- age_group  

### Transactions
- transaction_id  
- purchase_amount  
- shipping_type  
- purchase_frequency_days  

### Products
- item_purchased  
- category  
- season  
- size  

### Marketing & Behavior
- discount_applied  
- subscription_status  
- review_rating  

### Data Quality Actions

- Identified **37 missing review ratings**
- Imputed missing values using median per product category
- Standardized naming conventions to snake_case
- Engineered behavioral features
- Removed redundant variable (`promo_code_used`)

![Entity Relationship Diagram](images/erd.png)

---

# Executive Summary

From a revenue and marketing perspective, three critical insights emerge:

1. **Revenue concentration risk** — Clothing ($100K) and Accessories ($70K) dominate total revenue.
2. **Loyalty dependency** — 3,116 out of 3,900 customers are classified as Loyal.
3. **High discount penetration** — 43% of transactions involve discounts, with certain products reaching ~50%.

These findings directly influence promotional strategy, customer lifecycle planning, and subscription expansion opportunities.

![Dashboard Overview](images/dashboard_overview.png)

---

# Insights Deep Dive

---

## 1️⃣ Revenue & Product Performance

- Clothing generates approximately **$100K**, representing the primary revenue driver.
- Accessories follow with **$70K**, reinforcing category concentration.
- Footwear ($30K) and Outerwear ($10K) contribute significantly less.
- Male customers generate higher total revenue despite similar average transaction size, indicating frequency-driven behavior differences.

![Revenue by Category](images/revenue_by_category.png)

---

## 2️⃣ Customer Segmentation & Loyalty

Customer distribution:

- New: 83  
- Returning: 701  
- Loyal: 3,116  

Key Observations:

- Revenue reliance on loyal customers is substantial.
- Returning customers represent a conversion opportunity.
- Spending variability (Std Dev $23.69) suggests segmentation potential.

![Customer Segmentation](images/customer_segments.png)

---

## 3️⃣ Discount Sensitivity & Pricing Behavior

- Hat purchases: 50% discount-driven
- Sneakers: 49.66%
- Coats: 49.07%
- 43% of all transactions involve discounts

This level of promotional penetration suggests margin sensitivity and potential over-reliance on discounts.

![Discount Analysis](images/discount_analysis.png)

---

## 4️⃣ Subscription Impact & Revenue Distribution

- Subscriber revenue: **$62,645**
- Non-subscriber revenue: **$170,436**

Despite a strong loyal base, subscription penetration remains under-optimized.

![Subscription Revenue](images/subscription_analysis.png)

---

# Strategic Recommendations

Based on the analysis, the Marketing and Revenue Strategy teams should consider:

- Prioritizing investment in Clothing and Accessories due to revenue concentration.
- Replacing blanket promotions with targeted discount strategies.
- Developing structured conversion campaigns for returning customers.
- Enhancing subscription value proposition to increase recurring revenue.
- Improving service experience to elevate average review ratings beyond 4.0.

---

# Assumptions & Caveats

- Missing review ratings were imputed using median per category.
- Profit margin data was unavailable; analysis focuses on revenue.
- No deep seasonal segmentation was conducted.
- Discount impact measured at transaction level, not net profitability level.

---

# Repository Structure

```
customer-behavior-analysis/
│
├── data/
├── sql/
│   ├── data_cleaning.sql
│   └── business_queries.sql
├── images/
├── dashboard/
└── README.md
```

---

# Author

**Djibe Christian Diguina**  
Junior Data Analyst  
SQL • Python • Business Intelligence
