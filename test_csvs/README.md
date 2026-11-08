# Test CSVs for Nova Retail (Data tab → Upload → "Store and reprocess")

Select **all files of a set at once** when uploading. After each upload, check the Dashboard and Actions tabs: they refresh automatically.
"Reset to sample data" (Data tab) goes back to the demo shop between tests.

## Set A – clean data from a DIFFERENT shop ("Cairo Gadgets", P101–P106)
Upload `sales.csv`, `inventory.csv`, `customer_feedback.csv` together. Nothing from the sample shop should remain.
Expected (30-day dashboard, as of 2026-10-20): revenue **$18,254.79**, units **1021**, orders **392**, avg order **$46.57**, **3** products needing attention, avg rating **3.57**.
- Stock risk: Wireless Earbuds (stock 0) = critical, Power Bank 10000mAh (6.7 days vs 21-day lead time) = critical, Screen Protector = high.
- "What are my three most urgent business actions?" → top two: stockout of **Wireless Earbuds (P106)** and **Power Bank (P102)**, then Screen Protector review and the P103 quality-complaint investigation.
- "Best-selling products last month" → September 2026: Power Bank $5,822.67, Wireless Earbuds $4,379.27, Bluetooth Speaker $2,799.30.
- Old sample-shop proposals (USB-C Hub, Office Chair…) are retired automatically.

## Set B – same shop, different file format
`my_sales_export.csv`, `my_stock_report.csv`, `my_reviews.csv`: semicolon-separated, headers like `Invoice No / SKU / Qty / Price / On Hand / Vendor / Stars / Comment`, dates as dd/mm/yyyy.
Expected: the message lists every renamed column, and the dashboard numbers are **identical to Set A**.

## Set C – dirty rows (tests the rejection reasons)
Upload `sales_dirty.csv`, `feedback_dirty.csv` and Set A's `inventory.csv`. Expected rejected rows (Data tab):
| dataset | reason | detail |
|---|---|---|
| sales | bad_date | date '2026-13-45' is not a valid date |
| sales | bad_quantity | quantity '-3.0' must be a number >= 1 |
| sales | missing_value | empty: product_id |
| sales | bad_quantity | quantity '1.5' must be a whole number |
| sales | bad_unit_price | unit_price '0.0' must be a number >= 0.01 |
| sales | duplicate | duplicate of an earlier row |
| feedback | bad_rating | rating '9' is above the maximum allowed rating of 5 |
| feedback | missing_value | empty: rating |
| feedback | bad_rating | rating '0' must be a number >= 1 |
| feedback | bad_date | date 'not a date' is not a valid date |
| feedback | duplicate | duplicate of an earlier row |
Totals: sales 200/206 valid, feedback 41/46 valid.

## Set D – files that must be refused (your data must NOT change)
`random_not_business_data.csv` (not recognised), `sales_missing_price.csv` (names the missing column `unit_price`), `empty.csv`. Each says "Nothing was changed."

## Set E – ratings on a 1–10 scale
`customer_feedback_1to10.csv`: with the default `RATING_MAX = 5`, 81 of 120 rows are rejected and a warning tells you why. Set `RATING_MAX = 10` in the Agent 1 cell, run it, upload again: 120/120 valid (rescaled to 1–5).

## Mixing shops (warning test)
Upload only Set A's `sales.csv` onto the sample inventory → warning: "6 product_id(s) are not in the inventory file… Upload sales, inventory and feedback from the SAME shop together."
