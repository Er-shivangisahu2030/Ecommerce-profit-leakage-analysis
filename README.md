# E-Commerce Profit Leakage Analysis
## About This Project

This project looks at an e-commerce business where sales were strong but profit was not growing at the same pace. I wanted to find out where the money was being lost.

I cleaned and explored the data in Python, wrote the business queries in MySQL, and built a four-page Power BI dashboard to present the results. The data covers 50K orders.

## The Problem

Revenue looked healthy, but a few things were eating into profit:

- About 22% of orders were returned
- Return losses were very large
- Discounts were cutting into margins
- Cash on delivery (COD) orders seemed riskier than prepaid ones
- Refund delays and shipping costs added to the expense

The question I tried to answer: if revenue is high, why is profit not higher?

## What I Found

**Overall numbers**

| Metric | Value |
|---|---|
| Total revenue | ₹360.19M |
| Total profit | ₹90.86M |
| Profit margin | 25.23% |
| Return rate | 22.00% |
| Loss from returns | ₹40.74M |
| Total orders | 50K |

The ₹40.74M lost to returns is about 45% of the profit the business made.

**Categories and products**
- All four categories (Electronics, Beauty, Home, Fashion) earned about ₹22M to ₹23M profit each, so no single category was carrying the business
- Return rates were also close across categories, from 21.68% (Fashion) to 22.38% (Electronics)
- At product level, Mixer (23.05%), Laptop (22.91%) and Haircare (22.88%) had the highest return rates
- I listed the top 10 loss-making products so they can be repriced or removed

**Customers**
- Many customers returned half or more of their orders
- I built a list of these repeat returners by customer ID and city so they can be reviewed

**Payments**
- COD had the highest return rate (22.91%), followed by Prepaid (22.35%) and UPI (21.86%)
- UPI orders made the most average profit per order (₹57), compared with ₹39 for Prepaid and ₹37 for COD
- Google Ads brought in the most revenue (23.74%) and Instagram the least (16.05%)

**Operations**
- Return losses were highest in Delhi, Mumbai, Chennai and Ahmedabad (about ₹3.4M each), and lowest in Pune (₹2.86M)
- Orders with a delayed refund had a much higher return rate (100%) than orders without one (9.33%)
- Shipping cost was only 1.66% of revenue, so it is a small leak compared with returns

## Dashboard

**Page 1: Executive Overview**
Key numbers, monthly revenue and profit trend, profit by category, and return rate by category.


<img width="1106" height="714" alt="DASHBOARD PAGE-1" src="https://github.com/user-attachments/assets/18c7f70a-60ab-408b-8ae6-7d24cde7c41c" />


**Page 2: Product Intelligence**
Returns and profit by category and product, product return rates, the top 10 loss-making products, and discount vs profit.

<img width="1105" height="713" alt="DASHBOARD PAGE-2" src="https://github.com/user-attachments/assets/e8bd88bf-8649-4bfa-8852-0cdfb9788ec3" />


**Page 3: Customer Risk and Payment Analysis**
Return rate by payment type, customers with high return rates, revenue by acquisition channel, and average profit by payment type.

<img width="1105" height="713" alt="DASHBOARD PAGE-3" src="https://github.com/user-attachments/assets/5236f941-8383-4191-a298-578c701e6eb9" />

**Page 4: Operational Leakage**
Shipping cost as a share of revenue, return loss by city, effect of refund delays, and shipping cost vs order value.

<img width="1106" height="712" alt="DASHBOARD PAGE-4" src="https://github.com/user-attachments/assets/83f12e88-acb1-44d6-b4c6-190b103364d0" />

## Tools Used

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- MySQL
- Power BI (DAX, data modeling)
- Jupyter Notebook

## What the Business Could Do With This

- Review or remove the products that lose money
- Push customers toward UPI and prepaid payment, since those orders earn more
- Keep a closer watch on customers who return half or more of their orders
- Speed up refunds, since delays are linked to more returns
- Look at the cities with the highest return loss first

## What I Would Add Next

- A model to predict which orders are likely to be returned
- Customer clustering
- Cohort-based lifetime value analysis
- A what-if tool to test discount changes

## Author

Shivangi Sahu
Data Analyst | Power BI | SQL | Python
