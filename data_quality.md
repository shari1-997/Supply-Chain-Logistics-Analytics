# Data Quality & Preparation

This document records the data-preparation steps performed for the Power BI project.

## Source tables

The workbook includes Orders, Products, Suppliers, Warehouses, and Carriers, along with supporting data-quality notes and a data dictionary.

## Cleaning actions

- Promoted the first row to headers in the five core tables.
- Removed exact duplicate rows from Orders. The reported count moved from 3,025 source rows to 3,000 after deduplication.
- Filtered one invalid negative order quantity (`-5`, Order ID `ORD02158`), leaving 2,999 Orders rows in the cleaned query.
- Replaced missing Warehouse ID values with `Unknown`.
- Replaced missing Shipping Method values with `Unknown`.
- Retained missing Shipping Cost values as blank instead of inventing financial values.
- Cleaned descriptive text fields using Trim, Clean, and capitalization transformations where appropriate.
- Set date, whole-number, decimal-number, and text data types to match the fields.
- Checked Products for duplicate rows and duplicate Product IDs; no Product ID duplicates were found during the check.

## Known limitations

- Some Orders records have blank Actual Delivery Date values; these should not be treated as completed deliveries when calculating delivery duration or on-time delivery.
- Shipping Cost has missing values. A total based on `SUM` excludes blanks, so it represents recorded costs rather than an estimate of all costs.
- Unknown warehouse or shipping-method categories indicate missing source information, not a confirmed real-world category.
- The negative quantity was filtered out according to the project cleaning rule. In a production workflow, investigate the source record and document the correction or exclusion decision.

## Validation checklist

- [ ] Refresh the Power BI report after changing the source workbook.
- [ ] Confirm the row counts after each transformation.
- [ ] Validate key relationships and totals against the source data.
- [ ] Recheck measure definitions before using the report for operational decisions.
