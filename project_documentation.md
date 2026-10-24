# Project Documentation

## Project Summary
The **Supply Chain & Logistics Analytics Dashboard** is an interactive Power BI portfolio project for exploring order activity, delivery performance, supplier performance, order status, and shipping costs.

## Tools Used
- **Microsoft Excel** — source dataset
- **Power Query** — data cleaning and transformation
- **Power BI Desktop** — data model, DAX measures, visuals, and report pages

## Report Pages
1. **Overview** — key performance indicators, order status, orders by destination region, shipping cost by carrier, and monthly order trends.
2. **Supplier Performance** — supplier lead times and order value by supplier.
3. **Order Status** — order status distribution and delayed orders by region.
4. **Shipping & Cost Analysis** — recorded shipping costs by carrier and shipping method.

## Interactivity
The report includes slicers for **Month Name, Region, Shipping Method, Category, and Supplier Name**. Slicer behavior was checked across the report pages.

## Data Model
The **Orders** table is the central fact table and is related to lookup tables for Products, Suppliers, Warehouses, and Carriers. Review the relationships in Power BI Model view before changing the model or reusing it in another report.

## Key Measures
- **Total Orders** — distinct count of Order ID.
- **Total Order Value** — sum of Order Value.
- **Total Shipping Cost** — sum of recorded Shipping Cost values.
- **Average Delivery Days** — average elapsed days between Order Date and Actual Delivery Date for rows with an actual delivery date.
- **On-Time Delivery Rate** — eligible delivered orders arriving on or before the Promised Delivery Date, divided by eligible delivered orders.
- **Fulfillment Rate** — total shipped quantity divided by total ordered quantity.
- **Total Suppliers** — distinct supplier count, subject to the current report filters.

Measure values depend on the DAX definitions, data, and active filters. Check the measures in the PBIX file if you adapt the project.

## Files
The project folder contains the Power BI report (`.pbix`), a PDF export, the Excel source workbook, dashboard screenshots, and supporting Markdown documentation. The screenshots are stored in `Dashboard_ScreenShot/`.

## Open the Project
1. Install **Power BI Desktop**.
2. Open `Supply Chain & Logistics Analytics Dashboard.pbix`.
3. If Power BI requests the source workbook, browse to `Supply_Chain_Logistics_Raw_Dataset.xlsx` in the project folder. The workbook is in the project root, not in a `data/` subfolder.
4. Refresh the data, then check that the visuals and slicers load correctly.

## Data Quality and Limitations
The source data was cleaned before building the report. Exact duplicate order records were removed, one order with a negative order quantity was excluded, and missing shipping costs were left blank rather than replaced with invented values. Some actual delivery dates are also missing, so delivery metrics only reflect records eligible for those calculations. The dataset is intended for portfolio demonstration; observed patterns do not, by themselves, prove their causes.

See [data_quality.md](data_quality.md) for data-quality notes and [business_insights.md](business_insights.md) for findings shown by the dashboard.
