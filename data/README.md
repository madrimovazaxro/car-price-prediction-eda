# Data

| File | Rows | Description |
|---|---|---|
| `car_data_raw.csv` | 8,128 | Original, unmodified listings as published. |
| `car_data.csv` | 6,712 | De-duplicated, `"Test Drive Car"` listings removed, and unit-suffixed numeric columns (`mileage`, `engine`, `max_power`) converted to plain numbers. **This is the file the notebook loads.** |

## Source

[Vehicle dataset from CarDekho](https://www.kaggle.com/datasets/nehalbirla/vehicle-dataset-from-cardekho) — used-car listings scraped from [cardekho.com](https://www.cardekho.com), an Indian car marketplace.

## Columns (`car_data.csv`)

| Column | Type | Description |
|---|---|---|
| `name` | text | Full listing title (brand, model, trim) |
| `year` | int | Year of manufacture |
| `selling_price` | int | Asking price, in INR (₹) |
| `km_driven` | int | Total distance driven, in kilometers |
| `fuel` | text | Diesel / Petrol / CNG / LPG |
| `seller_type` | text | Individual / Dealer / Trustmark Dealer |
| `transmission` | text | Manual / Automatic |
| `owner` | text | First / Second / Third / Fourth & Above Owner |
| `mileage(km/ltr/kg)` | float | Fuel efficiency |
| `engine` | float | Engine displacement, in CC |
| `max_power` | float | Maximum power, in bhp |
| `seats` | float | Number of seats |

Further cleaning (extreme `km_driven` and `selling_price` outliers) is performed transparently inside the notebook, in **Section 5 — Data Cleaning**, so the full pipeline from raw data to final charts is reproducible end-to-end.
