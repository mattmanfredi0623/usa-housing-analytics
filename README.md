# USA Housing Analytics (Excel for the Web)

Cleaned and engineered a buyer‑friendly U.S. housing dataset using **Excel for the Web**.  
Features include **price per sqft**, **lot acres**, **years since last update**, and easy filters for **waterfront**, **basement**, **beds/baths**.  
Includes PivotTable summaries by city and ZIP for fast price/value comparisons.

## 🔍 Project Highlights
- **Engineered Features:** `price_per_sqft`, `lot_acres`, `home_age`, `years_since_update`, `waterfront_flag`, `basement_flag`, human‑readable labels for view/condition.
- **Buyer‑Centric Cleaning:** standardized addresses, split state/ZIP, fixed data types, removed duplicates/outliers.
- **Interactive Analysis:** PivotTables to compare **Average Price**, **Avg SqFt Living**, **Avg Price/SqFt** by city/ZIP with filters.

![Clean table overview](img/table_overview.png)
*Cleaned table with buyer-friendly columns*

## 🧰 Files
- `data/USA_Housing_Clean.csv` – **primary** cleaned dataset  
- `data/USA_Housing_Clean.xlsx` – Excel workbook (clean sheet, formulas, pivots)  
- `img/*.png` – screenshots for quick preview  
- `data_dictionary.md` – column definitions & formulas  
- `LICENSE` – MIT

## 🧪 How to Use
1. **Filter by location**: `city_clean`, `state`, `zip`
2. **Compare value**: sort by `price_per_sqft` (ascending = best value)
3. **Narrow by features**: `waterfront_flag`, `basement_flag`, `bedrooms`
4. **Time factors**: `home_age`, `years_since_update`, `last_reno_year`

## 📊 PivotTable Layout (Excel Web)
**Filters:** `waterfront_flag`, `basement_flag`, `bedrooms`, `state`/`zip`  
**Rows:** `city_clean` (optionally nest `zip`)  
**Values:** Average of `price`, Average of `sqft_living`, Average of `price_per_sqft`, Count of listings

> Sort Rows by **Average of price_per_sqft** to find best value areas.  
> Sort Rows by **Average of price** to see luxury markets.

![Pivot by city](img/pivot_by_city.png)
*Pivot: Average Price & Price/SqFt by city, filterable by beds, waterfront, basement*

## 🧹 Cleaning Steps (summary)
- Converted range to Table `Homes`, standardized data types (Currency for price; Date; Number for sqft)
- Split `statezip` → `state`, `zip`; normalized `street`/`city` with TRIM & PROPER
- Engineered features: 
  - `price_per_sqft = price / sqft_living`
  - `lot_acres = sqft_lot / 43560`
  - `home_age = YEAR(TODAY()) - yr_built`
  - `years_since_update = IF(yr_renovated>0, YEAR(TODAY())-yr_renovated, YEAR(TODAY())-yr_built)`
  - `waterfront_flag`, `basement_flag`
- Removed duplicates, flagged/deleted obvious outliers

## 💡 Notes
- Built 100% in **Excel for the Web** (no desktop Power Query).
- Ideal for buyers comparing neighborhoods, investors screening by price/sqft, and analysts building dashboards.

## 📄 License
MIT — free to use with attribution.
