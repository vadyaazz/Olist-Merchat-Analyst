# Olist-Merchat-Analyst

A small SQL project analyzing merchant performance on a public e-commerce marketplace dataset.

## Dataset

Brazilian E-Commerce Public Dataset by Olist (Kaggle). The raw CSV files are not included in this repository; please download them from Kaggle.

Tables used: `orders`, `order_items`, `sellers`, `products`, `product_category_name_translation`.

## Tools

- SQLite (DB Browser for SQLite). 
- Tableau for the Data Visualisation

## Business Questions and Findings

| # | Question | SQL techniques | Key insight |
| --- | --- | --- | --- |
| 1 | How do orders and revenue change month by month? | JOIN, GROUP BY, aggregation | Revenue grew rapidly from early 2017 and peaked in November 2017 at R$988K. 2016 data is very limited, so it is less representative. |
| 2 | Which 10 sellers generate the most revenue? | Multi-table JOIN, ORDER BY, LIMIT | The top seller is Guariba, with 1,124 orders and R$226,988 in revenue. Revenue does not always follow order volume: Lauro de Freitas ranks second with only 348 orders but R$217,940 in revenue, while Ibitinga has far more orders (1,772) but lower revenue at R$196,882. |
| 3 | How are sellers distributed across High / Mid / Low revenue segments? | CTE, CASE WHEN, subquery | About 9.5% of sellers (the High segment) generate 66% of total revenue, while over half of sellers (the Low segment) contribute only 4%. Sales are highly concentrated among a small group of top merchants, so retaining top sellers and helping Mid-segment sellers grow would have the biggest impact. |
| 4 | Which product categories perform best? | JOIN, LEFT JOIN, HAVING | Health & beauty is the top-selling category with about 1.23M in revenue. Categories grow in different ways: bed_bath_table has the most orders but a low average item price (93), while watches_gifts earns nearly the same revenue from far fewer orders thanks to a higher average price (199). |

## Author

Vadya Azzahra, Information Systems graduate.
