# 🛍️ Myntra Product Analytics Dashboard

*Excel Analytics & Interactive Reporting*

## Overview

- 🧹 Prepared and transformed raw product data to improve accuracy and usability
- 📈 Analyzed product pricing, discounts, brands, and categories using Pivot Tables and Excel formulas
- 🎯 Created an interactive dashboard with slicers for efficient filtering and trend visualization

## Tools Used

`Microsoft Excel` `Pivot Tables` `Slicers` `Data Cleaning` `Data Analysis`

## Dataset

- 24,000+ Product Records
- Myntra Fashion Dataset

## Dashboard Preview

<img width="1876" height="752" alt="Screenshot 2026-07-22 164804" src="https://github.com/user-attachments/assets/9baeb78f-a3e0-471d-9894-2fa5e99b7557" />


## Key Insights

### 1. Most expensive brand by marked price
> **EARNSHAW** — ₹44,950 for its *"Men Leather Straps Automatic Motion Watch"*

- **Method:** `MAX()` on marked price, filtered/grouped by brand

### 2. Brand with the maximum number of products sold
> **DressBerry** has the most products sold
*(Note: actual sales figures weren't available in the dataset, so rating count was used as a proxy for sales volume — a necessary assumption, flagged here for transparency.)*

 - **Method:** PivotTable — Brand × Sum(Rating Count)

### 3. Most selling product category
> **Perfume and Body Mist**

 - **Method:** PivotTable — Category × Sum(Rating Count)

### 4. Adidas vs. Nike vs. Mochi — which sold more?
> **Mochi** leads with ~1,477 products sold among the three

- **Method:** Filtered PivotTable (Brand IN {Adidas, Nike, Mochi}) × Sum(Rating Count)

### 5. Most popular product name
> **"Slim Fit Casual Shirt"** — appears ~260 times

- **Method:** `COUNTIF()` / PivotTable on Product Name

### 6. Brand with maximum discount (%)
> **Hritika** — up to **90.01%** discount

- **Method:** `MAX()` on discount %, grouped by brand

### 7. Product categories with negligible discount
> 13 categories show a **0.00%** maximum discount, including: key-chain, swim-tops, beard & moustache care, men's grooming kit, condoms, Patiala, free-gifts, rain-jacket, bibs, rain-suit, duvet-cover, shaving essentials, and robe

- **Method:** Filtered categories where `MAX(discount) = 0`

### 8. Categories with average discount above 70%
> **Anklets, Cufflinks, Floor Mats–Dhurries, and Patiala-and-Dupatta**

- **Method:** PivotTable — Category × Average(Discount %), filtered `> 70%`

