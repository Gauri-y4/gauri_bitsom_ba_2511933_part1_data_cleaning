# Part 1: Business Data Cleaning, Validation \& Excel Reporting

## Project Overview

This project focuses on cleaning, validating, and analyzing a retail sales dataset containing order-level information. The raw dataset included various data quality issues such as missing values, duplicate records, inconsistent text formatting, mixed date formats, invalid discounts, and shipping-related inconsistencies.

The objective was to create a clean and analysis-ready dataset, document all cleaning activities, and generate summary reports for business review.

---

## Business Objective

The objective of this project was to improve data quality by identifying and correcting inconsistencies, validating business rules, and preparing an analysis-ready dataset that supports accurate reporting and business decision-making.

---

## Dataset Used

Dataset File: raw_orders.xlsx

The dataset contains information related to:

* Customer details

* Product categories and sub-categories

* Sales and profit metrics

* Shipping information

* Order status and payment status


A cleaned version of the dataset was created as:

cleaned_orders.xlsx

---

## Tools and Technologies Used

• Microsoft Excel
• Pivot Tables
• Excel Functions and Formulas
• Data Validation
• Conditional Formatting

---

## Cleaning Steps Performed

### Text Cleaning

* Removed extra spaces and unnecessary formatting.

* Standardized capitalization and text values.

* Corrected inconsistencies in categorical fields such as region, category, and ship mode.


### Missing Value Handling

* Missing region values were replaced with "Unknown".

* Missing ship mode values were replaced with "Unknown".

* Missing discount values were replaced with 0 where applicable.


### Date Validation


* Standardized order_date and ship_date formats.

* Created shipping_delay_days to measure shipping time.

* Identified and flagged records where ship dates occurred before order dates.


### Duplicate Handling


* Removed exact duplicate records.

* Reviewed duplicate order IDs and flagged records with conflicting sales values.

### Business Rule Validation


* Flagged negative discount values.

* Validated shipping records.

* Created data quality flags for reporting and review.

### Calculated Columns Created


* cleaned_discount

* calculated_sales

* calculated_profit

* profit_margin

* shipping_delay_days

* order_month

* order_year

* data_quality_flag


---

## Business Rules Applied


* Missing region values were replaced with "Unknown".

* Missing ship mode values were replaced with "Unknown".

* Missing discounts were treated as 0 when appropriate.

* Negative discounts were flagged as invalid.

* Ship dates earlier than order dates were flagged as invalid.

* Duplicate order IDs with conflicting sales values were retained and flagged for review.

* Cancelled and returned orders were analyzed separately from completed orders.

---


## Data Quality Summary

| Issue                            | Count |

| -------------------------------- | ----: |

| Exact Duplicate Rows Removed     |    20 |

| Duplicate Order ID Pairs Flagged |    12 |

| Missing Discount Values Filled   |    18 |

| Negative Discount Records        |    15 |

| Invalid Shipping Records         |    93 |

| Clean Records                    |   784 |

| Invalid Records                  |   128 |

| Final Records After Cleaning     |   912 |


---


## Pivot Reports Created


The following pivot reports were generated:

1. Sales and Profit by Region

2. Sales and Profit by Category and Sub-Category

3. Order Count by Ship Mode

4. Profit Margin by Customer Segment

5. Cancelled and Returned Orders by Region

6. Monthly Sales Trend


---

## Key Business Insights

* Sales and profit performance varied across regions.

* Technology-related products contributed significantly to overall sales.

* Standard Class was the most frequently used shipping mode.

* Certain regions showed a higher concentration of cancelled and returned orders.

* Most data quality issues were related to shipping records and discount values.

---


## Assumptions


* Returned orders were treated as refunded orders for reporting purposes.

* Missing discount values represented no discount where other sales information was valid.

* Records with missing region or ship mode information were retained and categorized as "Unknown".


---

## Limitations

* The analysis was limited to the provided dataset.

* Duplicate order ID conflicts may require additional business review.

* Source-system level validation was outside the scope of this project.

---

## Repository Contents

### Data

* raw_orders.xlsx

* cleaned_orders.xlsx

### Outputs

* data_quality_report.xlsx

* pivot_summary.xlsx

* cleaning_log.md

### Screenshots

* raw_data_preview.png

* cleaned_data_preview.png

* pivot_summary_1.png

* pivot_summary_2.png

---


## Conclusion

The dataset was successfully cleaned, validated, and transformed into an analysis-ready format. Data quality issues were documented, business rules were applied, and reporting outputs were generated to support business decision-making.



