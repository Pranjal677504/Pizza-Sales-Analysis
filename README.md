# Pizza Sales Data Analysis Project (SQL)

## Project Overview
An end-to-end SQL database analysis project evaluating real-world pizza restaurant sales data. This project demonstrates database schema design, multi-table relationship mapping, and structural SQL analytics to derive actionable business insights regarding revenue performance, customer ordering behavior, and operational trends.

## Dataset Architecture
The relational database instance maps transaction histories across four primary structured datasets:
* **orders**: Tracks time-series data for customer entries (order_id, date, time).
* **order_details**: Relates unique transactional itemizations to their parent orders (order_details_id, order_id, pizza_id, quantity).
* **pizzas**: The structural product catalog defining sizing variants and unit costs (pizza_id, pizza_type_id, size, price).
* **pizza_types**: The descriptive master catalog outlining product taxonomy (pizza_type_id, name, category, ingredients).

---

## Technical Competencies Demonstrated
* **Database Normalization & DDL:** Executing programmatic schema initializations with optimal data types (DATE, TIME, INT), constraint applications (PRIMARY KEY), and explicit structure overrides.
* **Relational Operations:** Constructing clean multi-table INNER JOIN architectures to synthesize disparate flat files.
* **Data Aggregation:** Implementing comprehensive group metrics leveraging COUNT(), SUM(), AVG(), and ROUND() formatting.
* **Time-Series Analysis:** Applying operational time-extraction utilities (HOUR()) to map transactional velocity over the course of the business day.
* **Advanced Analytical SQL:** Formulating correlated Subqueries, inline derived tables, and robust Window Functions featuring RANK() OVER (PARTITION BY ... ORDER BY ...) metrics to isolate top performance tiers.

---

## Analytical Core: Strategic Business Insights Isolated

### Foundational Metrics
1. **Total Order Volume:** Evaluated overall transaction traffic across historical records.
2. **Gross Revenue Streams:** Determined structural cash flow margins derived from aggregate pricing and quantities.
3. **Menu Outliers:** Discovered premium pricing points within the core catalog to evaluate premium margins.
4. **Volume Consistency:** Modeled regular operational order quantities per customer basket.

### Tactical & Operational Insights
5. **Product Velocity:** Isolated the top 5 most frequently ordered menu selections along with cumulative transaction metrics.
6. **Peak Traffic Density:** Built hourly order distributions to locate high-volume operational waves (noting peak lunchtime cycles and steady dinner rushes).
7. **Menu Taxonomy Optimization:** Classified categorical pizza item popularity trends.
8. **Operational Yield Averages:** Developed data subqueries to model exactly how many pizza quantities move through fulfillment chains on a baseline standard day.
9. **Top Revenue Pillars:** Located the top 3 highest profit-yielding menu items.

### High-Tier Analytics
10. **Relative Revenue Allocation:** Computed exact percentage allocations per item category against overall gross income streams.
11. **Cumulative Financial Velocity:** Tracked structural rolling revenue accumulation over time using window functions.
12. **Tiered Section Rankings:** Designed layered ranking partitions to map the top 3 most profitable products inside each independent food category.

---

## Repository Files

| File | Contents |
|---|---|
| [orders.csv](orders.csv) | Order IDs, dates, and times |
| [order_details.csv](order_details.csv) | Ordered pizzas and quantities for each order |
| [pizzas.csv](pizzas.csv) | Pizza sizes and prices |
| [pizza_types.csv](pizza_types.csv) | Pizza names, categories, and ingredients |

## Implementation & Reproduction Workflow

This repository currently includes the four source CSV files and this README. Table-creation and analysis SQL scripts are not included.

1. Create a database named `pizza_hut` in your SQL client (for example, MySQL Workbench).
2. Create the `orders`, `order_details`, `pizzas`, and `pizza_types` tables using the CSV headers and the dataset architecture above. Choose appropriate data types and primary/foreign keys.
3. Import each linked CSV file into its matching table, treating the first row as column headers.
4. Write and run SQL queries for the analytical questions listed above. Save your schema and queries locally so you can repeat the analysis.
