# Sales Dashboard | Power BI

An interactive Power BI dashboard that analyses sales, profit and quantity across
products, categories, payment modes and sale types for **2024 – 2025**.

## Headline numbers

| Metric | Value |
|---|---|
| Total Sales (after discount) | 366.62K |
| Quantity Sold | 4,280 units |
| Profit | 34.1K |
| Profit % | ~10% |
| Transactions | 527 across 44 products |

## What the dashboard shows

**Slicers:** Year, Month, Sale Type, Payment Mode
**Sales & Profit by Month:** monthly trend for both measures
**Daily Sales:** day-of-month pattern
**Sales by Payment Mode:** Online vs Cash
**Sales by Sale Type:** Direct Sales, Online, Wholesaler
**Sales by Product** and **Sales by Category** (treemap)
## Key insights

**Discounts roughly halve profit.** Gross margin before discounts is about 68.9K, but
about 34.8K is given away in discounts, leaving 34.1K profit.
**Direct Sales drive the business:** 51.7% of sales, followed by Online (33.5%) and
Wholesaler (14.8%).
**Cash and online payments are almost evenly split** (49.5% / 50.5%).
**Top categories:** Personal Care (87.0K), Household (85.2K) and Beverages (83.6K).
Furnishing is the smallest at 47.6K.
## Data model

Two tables joined on PRODUCT ID (many-to-one, InputData → MasterData).

**InputData** (527 rows, transactions)

| Column | Description |
|---|---|
| DATE | Transaction date (2024-01-01 to 2025-12-31) |
| PRODUCT ID | Key to MasterData |
| QUANTITY | Units sold |
| SALE TYPE | Direct Sales / Online / Wholesaler |
| PAYMENT MODE | Cash / Online |
| DISCOUNT % | Discount applied to the line |

**MasterData** (44 products, reference)

| Column | Description |
|---|---|
| PRODUCT ID | Unique product key |
| PRODUCT | Product name |
| CATEGORY | Personal Care, Household, Beverages, Grocery, Furnishing |
| UOM | Unit of measure |
| BUYING PRIZE | Cost price per unit |
| SELLING PRICE | List price per unit |

Business logic: Sales = Quantity × Selling Price × (1 − Discount %) and
Profit = Sales − Quantity × Buying Price. 

## Tools

Power BI Desktop · DAX · Power Query · Excel

## 👤 Author

**Gowtham G**
Aspiring Data Analyst | SQL · Power BI · Python · Excel

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/your-linkedin-id)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/gowtham-g-2002)

⭐ If you found this project useful, consider giving the repo a star.
