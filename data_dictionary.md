# Data Dictionary

The raw Excel workbook contains five core tables. This dictionary describes the columns visible in the project workflow; refer to the workbook for the full set of source values.

## Orders

| Column | Meaning |
|---|---|
| Order ID | Unique order identifier |
| Order Date | Date the order was placed |
| Product ID | Product associated with the order |
| Supplier ID | Supplier associated with the order |
| Warehouse ID | Warehouse associated with the order; missing values were represented as `Unknown` during cleaning |
| Carrier ID | Carrier associated with the shipment |
| Order Quantity | Quantity ordered |
| Shipped Quantity | Quantity shipped |
| Unit Cost | Unit cost |
| Unit Price | Unit selling price |
| Order Value | Order value recorded in the source data |
| Shipping Cost | Recorded shipping cost; missing values remain blank |
| Shipping Method | Shipping method; missing values were represented as `Unknown` |
| Order Status | Current order status |
| Promised Delivery Date | Expected delivery date |
| Actual Delivery Date | Recorded actual delivery date; may be blank for orders without an actual delivery date |
| Destination Region | Destination region |

## Products

| Column | Meaning |
|---|---|
| Product ID | Product identifier |
| Product Name | Product name |
| Category | Product category |
| Supplier ID | Associated supplier identifier |
| Unit Cost | Product unit cost |
| Unit Price | Product unit price |
| Reorder Level | Quantity threshold used for replenishment |

## Suppliers

| Column | Meaning |
|---|---|
| Supplier ID | Supplier identifier |
| Supplier Name | Supplier name |
| Supplier Tier | Supplier classification/tier |
| Supplier Country | Supplier country |
| Lead Time Days | Supplier lead time in days |

## Warehouses

| Column | Meaning |
|---|---|
| Warehouse ID | Warehouse identifier |
| Warehouse Name | Warehouse name |
| City | Warehouse city |
| Region | Warehouse region |
| Capacity Units | Warehouse capacity in units |

## Carriers

| Column | Meaning |
|---|---|
| Carrier ID | Carrier identifier |
| Carrier Name | Carrier name |
| Transport Mode | Mode of transport |
| Service Level | Carrier service level |

> Note: Definitions above are based on the project table and column names. Confirm business-specific calculation rules with the source owner if this dataset is adapted for real operational use.
