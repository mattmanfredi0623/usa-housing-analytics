# Data Dictionary

| Column | Type | Description |
|---|---|---|
| date | Date | Record date |
| price | Currency | Sale/asking price |
| bedrooms | Number | Count of bedrooms |
| bathrooms | Number | Decimal baths (e.g., 2.5 = 2½) |
| sqft_living | Number | Finished living area (sqft) |
| sqft_lot | Number | Lot size (sqft) |
| floors | Number | Number of floors |
| waterfront | 0/1 | 1 = waterfront |
| view | 0–4 | Scenic rating (0 none → 4 excellent) |
| condition | 1–5 | 1 poor → 5 excellent |
| sqft_above | Number | Above-grade living area (sqft) |
| sqft_basement | Number | Basement area (sqft) |
| yr_built | Year | Year built |
| yr_renovated | Year/0 | Year of last renovation (0 = never) |
| street_clean | Text | Cleaned street address (TRIM/PROPER) |
| city_clean | Text | Cleaned city (TRIM/PROPER) |
| state | Text | State abbreviation |
| zip | Text | 5-digit ZIP |
| lot_acres | Number | `sqft_lot / 43560` |
| price_per_sqft | Currency | `price / sqft_living` |
| home_age | Number | `YEAR(TODAY()) - yr_built` |
| last_reno_year | Year/blank | Blank if never renovated |
| years_since_update | Number | Years since reno or build |
| waterfront_flag | Yes/No | Buyer-friendly label |
| basement_flag | Yes/No | Buyer-friendly label |
| bed_bath | Text | “3 bd | 2.5 ba” |
| view_label | Text | None/Fair/Good/Great/Excellent |
| condition_label | Text | Poor/Fair/Average/Good/Excellent |
