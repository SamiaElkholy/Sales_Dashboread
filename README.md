# Sales Performance Dashboard

An interactive Power BI dashboard that tracks revenue, cost, profit, and orders for a bicycle retailer, with a star-style data model built from a sales fact table and customer, region, and product dimension tables.

<img width="1322" height="735" alt="DataModling" src="https://github.com/user-attachments/assets/e9825b85-2286-4efa-93c0-2c6975de4728" />


## Key KPIs

| KPI | Value |
|---|---|
| Total Revenue | 425M |
| Total Cost | 250M |
| Total Profit | 175M |
| Profit Margin | 41.22% |
| Total Orders | 17K |

## Key Insights

1. **Bikes drive almost all of the profit:** the Bikes category generated 167M of the 175M total profit (about 95%), while Accessories contributed about 3.6%.
2. **Three subcategories dominate revenue:** Road Bikes (208M, about 49% of revenue), Mountain Bikes (150M), and Touring Bikes (52M) together make up about 96% of revenue. Tires and Tubes (4M) and Helmets (3M) are marginal.
3. **A small group of products carries a large share of sales:** the top 15 products generated 184M in revenue (about 43% of the total) and 77M in profit. Product 317 ranks first with 15.8M in revenue and 7.2M in profit.
4. **Data quality finding:** about 48% of revenue comes from sales whose customer key has no match in the customer table, so those sales cannot be assigned to a country. They are labeled **Unknown** in the country view instead of being dropped, so the revenue totals stay correct.

## Data Model

The model contains one sales fact table linked with one-to-many relationships to the dimension tables:

- `factSalesTable1` (sales fact table)
- `dimCustomerTable2` linked to `dimRegionTable4` (customer to region)
- `dimProductTable5` linked to `dimProductSubcategory` linked to `dimProductCategory` (product hierarchy)

## Dashboard Components

- **KPI cards:** Total Revenue, Total Orders, Total Cost, Total Profit, Profit Margin %
- **Profit By Category:** profit split across Bikes, Accessories, and Clothing
- **Top 15 Products:** ranked by revenue, with profit and order counts
- **Top 5 Subcategory Revenue:** revenue by product subcategory
- **Sales By Country:** revenue distribution by country, including an Unknown group

## Tools & Techniques

- **Power BI** for data modeling, report design, and interactive visuals
- **Power Query** for data cleaning and transformation
- **DAX** for measures and a calculated column that labels unmapped customers as Unknown



## Data Source

[Kaggel]

