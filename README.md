# E-commerce-Data-Engineering-Pipeline
This project demonstrates an end-to-end data pipeline using synthetic e-commerce data. It follows a medallion architecture (Bronze/Silver/Gold) and produces analytics-ready tables.
## Tech Stack
- Python, Pandas
- Parquet
- Jupyter Notebook
- Git/GitHub

## Data Layers
### Bronze (Raw)
- `bronze/customers.csv`
- `bronze/orders.csv`
- `bronze/order_items.jsonl` (nested items)

### Silver (Cleaned / Standardized)
- Standardized status values
- Parsed timestamps
- Handled missing values
- Exploded nested items into rows
Outputs:
- `silver/customers.parquet`
- `silver/orders.parquet`
- `silver/items.parquet`

### Gold (Analytics)
- Revenue by city
- Daily order counts
- Top products by quantity
Outputs:
- `gold/revenue_by_city.parquet` (+ CSV)
- `gold/daily_orders.parquet` (+ CSV)
- `gold/top_products.parquet` (+ CSV)

## How to Run
1. Generate data (Bronze): `notebooks/01_generate_bronze.ipynb`
2. Clean + explode (Silver): `notebooks/02_silver_cleaning.ipynb`
3. Analytics (Gold): `notebooks/03_gold_analytics.ipynb`

## Example Outputs
See files in the `gold/` folder.
