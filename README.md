# Intermediate SQL - Sales Analysis

## Overview

This analysis focuses on understanding customer behavior, revenue contribution, and retention patterns to identify growth opportunities and potential risks in the business.

## Business Questions

1. How is revenue distributed across different customer segments?
2. **Cohort Analysis:** How do different customer groups contribute to revenue over time?
3. What are the customer retention trends and churn patterns?

## Analysis Approach

### 1. Customer Segmentation Analysis

* Customers were segmented based on their total lifetime value (LTV)
* Segments created: High-value, Mid-value, and Low-value customers
* Key metrics calculated included total revenue contribution

🖥️ Query: [1_customer_segmentation.sql](1_customer_segmentation.sql)

📊 **Key Findings:**

* High-value segment (25% of customers) contributes 66% of total revenue ($135.4M)
* Mid-value segment (50% of customers) generates 32% of revenue ($66.6M)
* Low-value segment (25% of customers) contributes only 2% of revenue ($4.3M)

💡 **Business Insights:**

* **High-Value (66%)**: Introduce premium membership programs for 12,372 VIP customers, as losing even a few can significantly impact revenue
* **Mid-Value (32%)**: Develop targeted upgrade strategies through personalized offers, unlocking potential growth from $66.6M → $135.4M
* **Low-Value (2%)**: Launch re-engagement campaigns and price-sensitive promotions to boost purchase frequency

### 2. Cohort Analysis

* Revenue and customer count tracked across cohorts
* Cohorts grouped based on the year of first purchase
* Customer retention analyzed at the cohort level

🖥️ Query: [2_cohort_analysis.sql](/2_cohort_analysis.sql)

📊 **Key Findings:**

* Revenue per customer shows a consistent decline over time
* Cohorts from 2022–2024 are underperforming compared to earlier cohorts
* Total revenue growth is primarily driven by an increase in customer base, not higher customer value

💡 **Business Insights:**

* Customer value is declining over time, requiring deeper investigation
* A noticeable drop in customer acquisition occurred in 2023
* Declining LTV combined with reduced acquisition indicates potential future revenue risk

### 3. Customer Retention

* Identified customers with high churn risk
* Analyzed recency and purchase behavior
* Calculated customer-level retention metrics

🖥️ Query: [3_retention_analysis.sql](3_retention_analysis.sql)

📊 **Key Findings:**

* Cohort churn stabilizes around ~90% after 2–3 years, showing a predictable long-term pattern
* Retention rates remain consistently low (8–10%) across all cohorts, indicating a systemic issue
* Newer cohorts (2022–2023) follow similar churn trends, suggesting future cohorts may behave the same without intervention

💡 **Business Insights:**

* Focus on early-stage engagement (first 1–2 years) using onboarding incentives, loyalty programs, and personalized offers
* Prioritize win-back strategies for high-value churned customers to maximize ROI
* Implement predictive models to identify at-risk customers and intervene proactively


## Strategic Recommendations
1. Focus on increasing customer lifetime value by strengthening retention and early engagement strategies
2. Invest in personalized marketing to convert mid-value customers into high-value segments
3. Build predictive churn models to proactively retain valuable customers
4. Optimize acquisition strategies to ensure consistent inflow of high-quality customers

## Technical Details

* **Database:** PostgreSQL
* **Analysis Tools:** PostgreSQL, DBeaver, PGadmin