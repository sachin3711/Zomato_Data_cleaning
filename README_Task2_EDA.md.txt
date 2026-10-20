# Task 2: Exploratory Data Analysis (EDA) — Zomato Dataset

## Objective
Explore the cleaned Zomato menu dataset, calculate summary statistics, visualize patterns, and document useful insights.

## Dataset
- Rows: 152,740
- Columns: 12
- Date range: 2025-01-01 to 2025-08-31
- Missing values: 2 total, all in `Day wise` (2 rows)
- Numeric fields analyzed: `Price (INR)`, `Rating`, `Total Review`

## Key statistics
- Average listed price: ₹270.23; median: ₹229.00
- Average rating: 4.35/5; median: 4.4
- Average `Total Review`: 33.82; median: 10
- Veg: 114,029 rows (74.66%); Non Veg: 38,711 rows (25.34%)

## Useful insights
- **1. Food type mix:** Veg items account for 74.66% of rows (114,029), while Non Veg accounts for 25.34% (38,711). This describes dataset composition, not actual orders or sales.
- **2. Rating distribution:** The average rating is 4.35/5 and median is 4.4. 85.52% of rows have ratings above 4.0.
- **3. Price distribution:** Average listed price is ₹270.23; median is ₹229.00. The average exceeds the median, consistent with a right-skewed distribution influenced by high-priced group/party items.
- **4. Day-wise pattern:** Saturday has the most rows (22,598) and Tuesday the fewest (21,212). These are dataset row counts by day, not confirmed orders.
- **5. City representation:** Bengaluru has the most rows (20,077) among cities in the dataset. This may reflect data coverage rather than market demand.
- **6. Monthly coverage:** The data spans 2025-01-01 to 2025-08-31. Monthly row counts vary within a relatively narrow range; compare coverage before interpreting this as demand.
- **7. Price anomaly candidates:** The maximum listed price is ₹8,000.00; the 99th percentile is ₹1,199.00. High values include party/large-serving menu items, so they should be reviewed in context rather than automatically deleted.

## Visualizations
The accompanying Excel workbook contains charts for:
1. Dataset rows by food type
2. Rows by day of week
3. Dataset rows by month
4. Rows by rating band

## Important interpretation limits
This dataset appears to be menu/listing-level data. Row counts are not necessarily orders, revenue, or customer demand. `Total Review` is treated as a field in the dataset, not as a transaction count. High listed prices may be party packs or multi-person combos; they are flagged for contextual review rather than automatically labeled errors. Two rows have missing `Day wise`; inspect or derive this field from `Order Date` before further analysis if appropriate.

## Files
- `zomato_clean_Dataset.xlsx` — cleaned source dataset
- `Zomato_EDA_Analysis.xlsx` — summary statistics, grouped counts, charts, and written insights
- `README_Task2_EDA.md` — project documentation
