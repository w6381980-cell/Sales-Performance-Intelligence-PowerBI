📊 Sales & Profit Intelligence Dashboard (Power BI)
🔍 Project Overview

This project is an enterprise-grade Power BI dashboard designed to analyze Sales, Profit, Loss, Discounts, and Regional Performance using realistic business data.
The dashboard follows industry best practices including clean UI, synced slicers, advanced DAX, and executive-level storytelling.

This project is suitable for:

Entry-Level Data Analyst portfolios

LinkedIn & GitHub showcase

Client demos & interviews

Power BI industrial use-cases

🧱 Data Model

Fact Table

Sales_Fact_Table

Sales

Profit

Discount %

Quantity

Cost Amount

Product ID

Customer ID

Date

Dimension Tables

Product_Table

Customer_Table

Calendar_Table

Star schema modeling is used for optimal performance.

📄 Report Pages (6 Pages)
🔹 Page 1: Sales & Profit Overview

Purpose: High-level business performance

Visuals:

Line Chart → Monthly Sales Trend

Bar Chart → Profit by Category

Table → Top 10 Products

Map → Sales by State (India)

Slicers (Synced):

Year

Category

🔹 Page 2: Customer & Category Insights

Purpose: Customer distribution & category contribution

Visuals:

Stacked Column → Sales vs Profit by Category

Donut Chart → Customer Distribution by Segment

Table → Top Customers by Sales & Profit

🔹 Page 3: Loss-Making Products & Regions

Purpose: Identify negative performance areas

Visuals:

Table → Loss by Product / State

KPI → Total Loss Amount

Conditional Formatting → Red for losses

🔹 Page 4: Discount Impact Analysis (Advanced)

Purpose: Understand why losses occur

Visuals:

Scatter Chart → Discount % vs Profit

X-Axis: Discount % (Column)

Y-Axis: Total Profit

Size: Total Sales

Details: Discount Band

📌 Shows how higher discounts impact profitability.

🔹 Page 5: Executive Summary / CEO View

Purpose: Board-level decision support

Visuals:

KPI Cards → Sales, Profit, Loss %, Growth

Shape Map (India) → Profit by State

Donut → Sales Contribution by Category

📌 Answers:

Which regions need intervention?

Is the business over-dependent on one category?

🔹 Page 6: Immediate Action Required

Purpose: Decision-making & risk control

Visuals:

Table → Loss % by Category & State

Conditional Formatting:

Deep Red background for losses

White text

Minimal slicer usage (Year only – optional)

🎛️ Slicer Strategy (Enterprise UX)

Only 2 slicers used:

Year

Category

Slicers are:

Synced across all 6 pages

Visible only on Page-1

Clean UI with global filter control

🧮 Key DAX Measures
Total Sales
Total Sales = SUM(Sales_Fact_Table[Sales])

Total Profit
Total Profit = SUM(Sales_Fact_Table[Profit])

Loss Amount
Loss Amount =
IF(
    Sales_Fact_Table[Profit] < 0,
    Sales_Fact_Table[Profit],
    BLANK()
)

Loss %
Loss % =
DIVIDE([Total Profit], [Total Sales])

Discount Band
Discount Band =
SWITCH(
    TRUE(),
    Sales_Fact_Table[Discount %] <= 0.10, "0–10%",
    Sales_Fact_Table[Discount %] <= 0.30, "10–30%",
    Sales_Fact_Table[Discount %] <= 0.50, "30–50%",
    "50%+"
)

🎨 Design & UX

Dark professional theme

Green → Profit

Red → Loss

Clean navigation buttons

Image-based headers (online URLs)

Fully interactive visuals

🚀 Tools & Skills Used

Power BI

DAX

Data Modeling (Star Schema)

Business Intelligence

Data Visualization

Executive Reporting

📌 Author

Hardik Jaiswal
Entry-Level Data Analyst
Skills: Power BI | SQL | Excel | Python
