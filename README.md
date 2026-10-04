# Excel Chocolate Sales Analysis

I built this project in Excel to analyze 1,094 chocolate sales transactions and turn the raw data into an interactive reporting workbook.

While reviewing my original version, I found a data-quality issue: some dates in the finished workbook had been changed and extended the analysis beyond the source period. The raw source only covers **January to August 2022**, so I rebuilt the analysis from the untouched source data before improving the dashboard.

That review also caught a mislabeled metric. `Amount ÷ Boxes Shipped` had previously been called **Cost per Box**, but the calculation is actually **Revenue per Box**. The upgraded workbook uses the correct label.

## Main results

- **Total revenue:** $6,183,625
- **Boxes shipped:** 177,007
- **Orders:** 1,094
- **Average order value:** $5,652
- **Revenue per box:** $34.93
- **Top market:** Australia — $1.14M
- **Top product:** Smooth Silky Salty — $349.7K
- **Top sales rep:** Ches Bonnell — $320.9K
- **Strongest month:** January — $896.1K
- **Standard orders:** about 69.7% of transactions

## What is inside the workbook

### Dashboard

A high-level view of the main KPIs, top products and monthly revenue trend.

### Interactive View

This sheet lets the user filter the analysis with dropdowns for:

- Country
- Product
- Sales Person
- Order Size

The selections update revenue, order count, boxes shipped, average order value, revenue per box and monthly results.

The logic is formula-driven using multi-criteria `SUMIFS` and `COUNTIFS`, rather than manually changing the source data.

### Performance Analysis

I added a deeper comparison layer for products, salespeople and countries, including:

- Revenue
- Orders
- Boxes shipped
- Average order value
- Revenue per box
- Revenue share
- Revenue ranking
- Conditional formatting and data bars
- Country-by-month performance
- Sparklines for monthly trends

The workbook also uses `INDEX`/`MATCH` and ranking formulas to return the position of selected products and salespeople.

### Scenario Planning

The scenario sheet adds a simple business-planning layer.

A user can choose a revenue growth target and the workbook calculates:

- Target revenue
- Incremental revenue required
- Required average order value
- Additional boxes needed at the current revenue-per-box level
- Revenue targets and gaps by country
- Monthly country targets

This keeps the project from being only a historical dashboard and shows how Excel can also be used for planning.

### Data Audit

Before the analysis, I checked the source for:

- Missing values
- Exact duplicate rows
- Date range
- Non-positive revenue
- Non-positive boxes shipped

The audit also documents the product spelling correction and the Revenue per Box metric correction.

## Workbook structure

| Sheet | Purpose |
|---|---|
| Chocolate Sales | Original source data |
| Analysis Data | Clean analysis table and derived columns |
| Summary | Formula-based KPI and aggregation layer |
| Dashboard | Main reporting view |
| Data Audit | Source-data quality checks |
| Interactive View | User-controlled filtered analysis |
| Performance Analysis | Product, salesperson and country comparisons |
| Scenario Planning | Revenue growth what-if analysis |
| _Lists | Supporting values for dropdown controls |

## Excel skills used

- Excel Tables
- Data validation and dropdown controls
- `SUMIFS`
- `COUNTIFS`
- `IF` / `IFERROR`
- `INDEX` + `MATCH`
- `RANK.EQ`
- Absolute and relative cell references
- KPI calculations
- Dynamic charts
- Conditional formatting
- Data bars and color scales
- Sparklines
- What-if / scenario analysis
- Data-quality auditing

## Files

- **`chocolate sales.xlsx`** — original source workbook
- **`chocolate sales analysis.xlsx`** — upgraded analysis workbook

## Data scope

The dataset contains **1,094 transactions from 3 January 2022 to 31 August 2022**.

I kept the source data unchanged and built the analysis on a separate working sheet so the cleaning and derived calculations can be reviewed without overwriting the original records.

## Notes

This project is focused on Excel analysis and reporting. It does not contain product cost or profit data, so I do not make profit-margin claims from the dataset.
