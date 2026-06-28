\# Data Cleaning Log



\## Issues Found



While reviewing the dataset, several data quality issues were identified:



\* Missing values were found in the region, ship\_mode, and discount columns.

\* Some text fields contained extra spaces and inconsistent capitalization.

\* Order and shipping dates were stored in different formats.

\* Exact duplicate records were present in the dataset.

\* Some order IDs appeared more than once with different sales values.

\* A few records contained negative discount values.

\* Several records had ship dates that occurred before the corresponding order dates.



\## Cleaning Actions Performed



The following cleaning steps were carried out:



\* Standardized text fields by removing unnecessary spaces and correcting formatting inconsistencies.

\* Replaced missing region values with "Unknown".

\* Replaced missing ship\_mode values with "Unknown".

\* Filled missing discount values with 0 where appropriate.

\* Converted order\_date and ship\_date into a consistent date format.

\* Created a shipping\_delay\_days column to calculate delivery time.

\* Removed exact duplicate records.

\* Flagged duplicate order IDs that had conflicting sales values for further review.

\* Flagged invalid discount records.

\* Flagged records where the ship date was earlier than the order date.

\* Created additional calculated columns to support analysis and reporting.



\## Business Rules Applied



The following business rules were applied during the cleaning process:



\* Missing region values were replaced with "Unknown".

\* Missing ship\_mode values were replaced with "Unknown".

\* Missing discount values were treated as 0 when the remaining sales information was valid.

\* Negative discount values were flagged as invalid.

\* Discounts above the acceptable range were checked and none were found.

\* Records with ship dates earlier than order dates were flagged as invalid shipping records.

\* Duplicate order IDs with conflicting sales values were retained but flagged for review.

\* Cancelled and returned orders were reported separately from completed orders.



\## Assumptions Made



\* Returned orders were treated as refunded orders for reporting purposes.

\* Missing discount values indicated that no discount had been applied.

\* Records containing missing region or ship mode information were retained and categorized as "Unknown" rather than being removed.



\## Records Removed



\* 20 exact duplicate records were removed from the cleaned dataset.



\## Records Flagged



\* 12 duplicate order ID pairs were flagged for review.

\* 93 records were flagged due to invalid shipping dates.

\* 15 records were flagged because of negative discount values.



\## Limitations



\* The analysis was limited to the information available in the provided dataset.

\* Conflicting duplicate order IDs may require additional business validation.

\* Any issues originating from the source systems could not be independently verified.



