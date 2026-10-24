# Supply Chain & Logistics Analytics Dashboard --- Power BI

An interactive Power BI project exploring order activity, delivery
performance, supplier performance, and shipping costs.

![Supply Chain & Logistics Dashboard ---
Overview](Dashboard_ScreenShot/Overview.jpg)

## Dashboard Preview

The report contains four pages:

  -----------------------------------------------------------------------
  Page                                What it covers
  ----------------------------------- -----------------------------------
  **Overview**                        Key performance indicators, order
                                      status, orders by destination
                                      region, shipping cost by carrier,
                                      and monthly order trends

  **Supplier Performance**            Total suppliers, supplier lead
                                      times, and order value by supplier

  **Order Status**                    Order-status distribution and
                                      delayed orders by region

  **Shipping & Cost Analysis**        Total shipping cost, shipping cost
                                      by carrier, and shipping cost by
                                      shipping method
  -----------------------------------------------------------------------

### Other dashboard pages

**Supplier Performance**

![Supplier Performance
dashboard](Dashboard_ScreenShot/Supplier%20Performance.jpg)

**Order Status**

![Order Status dashboard](Dashboard_ScreenShot/Order%20Status.jpg)

**Shipping & Cost Analysis**

![Shipping & Cost Analysis
dashboard](Dashboard_ScreenShot/Shipping%20%26%20Cost%20Analysis.jpg)

## Key Metrics Shown

The report includes measures such as:

-   Total Orders
-   Total Order Value
-   On-Time Delivery Rate
-   Total Shipped Quantity
-   Average Delivery Days
-   Fulfillment Rate
-   Total Shipping Cost
-   Total Suppliers
-   Average Lead Time by Supplier

Values shown on the dashboard reflect the report's current filters and
data.

## Interactive Features

Use the report slicers to explore results by:

-   Month
-   Region
-   Shipping Method
-   Product Category
-   Supplier Name

The slicers are intended to filter the report visuals and support
comparisons across different parts of the supply chain.

## Project Files

  -----------------------------------------------------------------------------------------
  File                                                  Description
  ----------------------------------------------------- -----------------------------------
  `Supply Chain & Logistics Analytics Dashboard.pbix`   Power BI Desktop report; open this
                                                        file to explore or edit the
                                                        dashboard

  `Supply Chain & Logistics Analytics Dashboard.pdf`    PDF export of the dashboard

  `Supply_Chain_Logistics_Raw_Dataset.xlsx`             Excel dataset used for the project

  `Dashboard_ScreenShot/`                               Screenshots of all four report
                                                        pages

  `project_documentation.md`                            Project overview and documentation

  `business_insights.md`                                Summary of business insights

  `data_dictionary.md`                                  Dataset fields and their meanings

  `data_quality.md`                                     Data-cleaning and quality notes

  `.github/`                                            GitHub repository configuration and
                                                        templates, if included
  -----------------------------------------------------------------------------------------

## Data Preparation

The project uses Power Query to prepare the data before analysis. The
documented preparation includes promoting headers, removing exact
duplicate order records, standardizing text fields, setting appropriate
data types, replacing missing warehouse and shipping-method values with
`Unknown`, retaining missing shipping costs rather than inventing
financial values, and excluding a record with a negative order quantity.

Refer to [`data_quality.md`](data_quality.md) and
[`data_dictionary.md`](data_dictionary.md) for the project's detailed
notes.

## Tools Used

-   **Microsoft Power BI Desktop** --- data modeling, DAX measures,
    visuals, and report design
-   **Power Query** --- data cleaning and transformation
-   **Microsoft Excel** --- source dataset
-   **Markdown and GitHub** --- project documentation and presentation

## How to View the Project

1.  Open the PDF for a quick, read-only preview.
2.  To interact with the report, open
    `Supply Chain & Logistics Analytics Dashboard.pbix` in Power BI
    Desktop.
3.  If you are reviewing the project on GitHub, use the screenshots
    above to preview the report pages.

## Repository Structure

``` text
02_Supply_Chain_&_Logistics_Analytics/
├── .github/
├── Dashboard_ScreenShot/
│   ├── Overview.jpg
│   ├── Supplier Performance.jpg
│   ├── Order Status.jpg
│   └── Shipping & Cost Analysis.jpg
├── .gitignore
├── README.md
├── business_insights.md
├── data_dictionary.md
├── data_quality.md
├── project_documentation.md
├── LICENSE_NOTE.txt
├── Supply Chain & Logistics Analytics Dashboard.pbix
├── Supply Chain & Logistics Analytics Dashboard.pdf
└── Supply_Chain_Logistics_Raw_Dataset.xlsx
```

## Notes

-   This is a portfolio and analytics project. Dashboard figures should
    be interpreted in the context of the dataset and the selected
    filters.
-   Before making the repository public, review the dataset and files to
    ensure you have permission to share them and that they contain no
    confidential or personal information.
-   No open-source license is declared by this README. Add a `LICENSE`
    file only if you have decided which license applies to your work.

------------------------------------------------------------------------

**Created as a Power BI portfolio project focused on supply chain and
logistics analytics.**
