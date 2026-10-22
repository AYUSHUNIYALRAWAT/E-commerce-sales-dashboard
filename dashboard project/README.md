# E-commerce Sales Dashboard \| Power BI

> **Turning e-commerce transactions into a business story.**

This Power BI project explores how sales, profit, order quantity,
average order value, product categories, payment methods, customers, and
geography work together to shape e-commerce performance.

## The business story

An e-commerce business needs more than a sales total to understand
whether it is performing well. Revenue can look healthy while profit is
weak, and popular products do not always generate the strongest returns.
This dashboard brings several views of performance together so a user
can move from **"What happened?"** to **"Where should we investigate?"**

### 1. Start with the headline KPIs

The dashboard highlights four top-level measures:

  -----------------------------------------------------------------------
  KPI                     What it tells us        Business question
  ----------------------- ----------------------- -----------------------
  **Total Sales /         The overall value of    How much business did
  Amount**                sales represented in    we generate?
                          the dataset             

  **Total Profit**        The profit recorded     Are sales translating
                          across transactions     into profit?

  **Quantity Sold**       The quantity of items   How much product volume
                          sold                    are we moving?

  **Average Order Value   Average value per       How much value does a
  (AOV)**                 order, as defined by    typical order
                          the data model          contribute?
  -----------------------------------------------------------------------

These KPIs should be read together. For example, rising sales with
falling profit may signal a need to investigate product mix, discounts,
costs, or other margin pressures. A higher AOV may indicate larger
baskets, but it should be interpreted alongside order volume and profit.

> **KPI note:** The `.pbix` file defines the KPI visuals, but this
> README does not state numerical results because those values have not
> been independently extracted and verified here. Open the report in
> Power BI to read the current figures.

## 2. Explore the drivers behind performance

### Profit over time

The monthly profit visual helps reveal how profitability changes across
the reporting period. Use it to spot peaks, dips, and periods that
deserve a closer look. A single month should not be treated as a trend
without comparing it with other periods.

### Profit by sub-category

The sub-category chart breaks profit down into more detailed product
groups. This helps identify which parts of the catalogue appear to
contribute more or less profit and where product-level investigation may
be useful.

### Quantity by category

The category view compares sales volume across broad product groups. It
complements the profit view: a category that sells many units is not
automatically the category that contributes the most profit.

### Profit by payment mode

The payment-mode chart compares profit across payment methods. This is
useful for exploring the transaction mix, but differences alone do not
prove that a payment method causes higher or lower profit.

### Average order value by state

The geographic comparison explores AOV across states. It can help
identify regional differences and generate questions about customer
baskets, local demand, and market opportunities. State comparisons
should be interpreted in light of the number of orders and the period
selected.

### Sales amount by customer

The customer chart shows sales amount across customers, helping users
explore customer-level contribution and identify where concentration may
exist. High sales contribution is not the same as high profitability or
customer loyalty.

## 3. Interact with the report

The report includes slicers for:

-   **Quarter** --- narrow the analysis to a selected quarter.
-   **State** --- focus the analysis on a geographic market.

Use the slicers to compare periods and regions. When filtering, review
all KPIs and visuals together rather than drawing a conclusion from one
chart in isolation.

## A practical analysis workflow

1.  **Check the headline KPIs.** Establish the sales, profit, quantity,
    and AOV baseline.
2.  **Choose a quarter or state.** Narrow the report to the business
    segment you want to understand.
3.  **Inspect the time trend.** Look for changes in monthly profit and
    note periods that need explanation.
4.  **Compare product performance.** Review profit by sub-category
    alongside quantity by category.
5.  **Review customer and payment patterns.** Use these views to
    generate hypotheses, not to assume causation.
6.  **Turn observations into actions.** Validate any apparent
    opportunity against transaction-level data, costs, discounts, and
    order counts before recommending a business change.

## KPI definitions and interpretation

-   **Sales / Amount:** The report's total of `Details.Amount`.
-   **Profit:** The report's total of `Details.Profit`.
-   **Quantity:** The report's total of `Details.Quantity`.
-   **AOV:** The report uses the `Details.AOV` field. Confirm how this
    field is calculated in the underlying model before comparing it with
    an independently calculated average order value.
-   **Profit by month:** Aggregates `Details.Profit` across the month
    hierarchy of `Orders.Order Date`.
-   **Profit by sub-category:** Aggregates profit by
    `Details.Sub-Category`.
-   **Quantity by category:** Aggregates quantity by `Details.Category`.
-   **Profit by payment mode:** Aggregates profit by
    `Details.PaymentMode`.
-   **AOV by state:** Aggregates AOV by `Orders.State`.
-   **Sales by customer:** Aggregates amount by `Orders.CustomerName`.

## Key business questions this dashboard helps investigate

-   Is the sales total accompanied by healthy profit?
-   Which sub-categories contribute most and least to profit?
-   Do high-volume categories also contribute strongly to profit?
-   How does monthly profit vary over time?
-   How does AOV differ across states?
-   Is sales value concentrated among a small number of customers?
-   Do payment-mode patterns change when the quarter or state filter
    changes?

These are **questions for analysis**, not claims about the results. The
actual answer depends on the selected filters and the underlying data.

## Tools and skills demonstrated

-   **Power BI** --- interactive dashboard design and report navigation
-   **KPI reporting** --- sales, profit, quantity, and average order
    value
-   **Business analysis** --- product, customer, time, payment, and
    geographic breakdowns
-   **Data storytelling** --- connecting summary metrics with diagnostic
    views
-   **Interactive filtering** --- quarter and state slicers

## Suggested next improvements

To make the dashboard even more decision-ready, consider adding:

-   Sales and profit trends together, with year-over-year or
    period-over-period change
-   Profit margin (`Profit / Sales`) and an explicit order count
-   Targets or benchmarks for sales and profit
-   Top and bottom product sub-categories by profit
-   A tooltip with sales, profit, quantity, margin, and order count
-   Clear reporting-period context and a data-refresh date
-   A data dictionary explaining the calculation behind AOV and the
    treatment of returns, discounts, and costs

## How to use

1.  Download or clone this repository.
2.  Open `E-commerce sales dashboard.pbix` in Microsoft Power BI
    Desktop.
3.  Wait for the report to load and use the **Quarter** and **State**
    slicers to explore the data.

## Project takeaway

This dashboard is designed to tell a connected performance story:
**sales show business scale, profit shows financial contribution,
quantity shows product movement, and AOV adds context about order
value.** The supporting product, customer, payment, time, and state
views help users investigate what may be driving those results before
deciding what to do next.

------------------------------------------------------------------------

*Built as a Power BI e-commerce analytics project. Numerical findings
should be added only after validating the figures shown by the report
and documenting the dataset's definitions.*
