# Stripe Connect Payout Behavior Analysis

**Prepared by: Khalid**  
**Email:** kshaikhq@uwaterloo.ca

---

## Executive Summary

This document presents an analysis of Stripe Connect's payout patterns to estimate future payouts and identify growth opportunities. It highlights the anticipated payouts for each country on January 1, 2019, and identifies significant regional variances. Key industries such as Education, Food & Beverage, and Hotels, Restaurants & Leisure are projected to show notable payout growth in 2019. Recommended metrics for ongoing tracking include Gross Payment Volume (GPV), Net Revenue, and Active Platform Engagement.

---

## Objective and Data Overview

**Objective:**  
Leverage historical payout data to forecast future performance and identify key operational metrics.

**Data Sources:**

- **payouts.csv:** Daily payout amounts, with platform and recipient IDs.
- **countries.csv:** Mapping of merchant IDs to countries.
- **industries.csv:** Mapping of merchant IDs to industries.

Stripe Connect allows platform businesses to pay out money to other businesses globally. This project analyzes the payout behavior of Stripe platforms.

---

## Analytical Approach

### Data Preparation

1. Explore the datasets.
2. Check for missing values and outliers.
3. Perform imputation.
4. Clean and merge datasets to form a comprehensive view of payouts by country and industry.

### Forecasting Method

- Utilize time series analysis for estimating country payouts.
- Use linear regression with seasonal dummy variables.
- Apply industry growth rates to project 2019 volumes.

### Metrics Definition

- Gross Payment Volume (GPV)
- Net Revenue
- Active Platform Engagement

---

## Problem 1: Estimating Payouts for Jan. 1, 2019

**Forecast Methodology:**  
Estimates are based on historical payout trends, adjusted for seasonal variations and growth patterns using seasonal ARIMA (Time-series forecasting).

### Country-wise Forecast

| Country | Unique Platforms | Unique Recipients | Forecasted Payout for Jan 1, 2019 ($) | Payout % |
|---------|------------------|-------------------|--------------------------------------|----------|
| US      | 229              | 55385             | $4,842,832                           | 88.29%   |
| GB      | 49               | 2899              | $253,066                             | 4.61%    |
| FR      | 45               | 22850             | $106,512                             | 1.94%    |
| CA      | 25               | 1417              | $83,825                              | 1.53%    |
| AU      | 33               | 1397              | $65,371                              | 1.19%    |
| Others  | -                | -                 | -                                    | -        |

---

## Problem 2: Projected Payout Volumes for 2019

### Projection Method

1. Calculate the average daily payout for each industry.
2. If the industry was present in 2018, use its average daily payout for projection.

**Assumption:** Linear growth without accounting for potential market dynamics.

### Industry-wise Projection

| Industry                | Average Daily Payout per Platform in 2018 | Number of Future Platforms | Estimated Total Daily Payout Volume for 2019 |
|-------------------------|-------------------------------------------|----------------------------|----------------------------------------------|
| Food & Beverage         | $7,704.08                                 | 40                         | $308,163.03                                  |
| Education               | $16,390.32                                | 15                         | $245,854.74                                  |
| Hotels, Restaurants & Leisure | $0.94                              | 5                          | $4.70                                        |

Total estimated daily payout volume on a typical day for the selected industries in 2019: $554,022.47

---

## Problem 3: Key Metrics for Stripe Connect

### Metrics

1. **Gross Payment Volume (GPV):** Total volume of payouts processed through Stripe Connect.
2. **Average Payout Size:** Average amount of money transferred per payout.
3. **Payout Growth Rate:** Rate of growth in total payout volume from one period to the next.
4. **Active Platforms:** Number of unique platforms that have made at least one payout in a given period.
5. **Payout Frequency by Platform:** Average number of payouts initiated by each platform.
6. **Platform and Recipient Churn Rate:** Rate at which platforms or recipients stop using Stripe Connect for payouts.
7. **Net Revenue from Payouts:** Revenue Stripe earns from processing payouts, after deducting costs.
8. **Active Recipients:** Number of unique recipients that have received at least one payout in a given period.
9. **RFM Score:** Enhancing platform loyalty with RFM segmentation.

---

## Conclusion

The analysis provides strategic insights into Stripe Connect's payout behavior, projecting significant growth in key industries for 2019 and identifying crucial metrics for ongoing performance tracking. These insights empower data-driven decision-making to optimize growth and operational efficiency.

---
