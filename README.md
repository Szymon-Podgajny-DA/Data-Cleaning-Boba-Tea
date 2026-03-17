# DA-Portfolio-Data-Cleaning-Boba-Tea
Cleaned a boba tea shop dataset in spreadsheets by removing duplicates, fixing invalid ratings, and restructuring columns into an analysis-ready table.

# Data Cleaning – Boba Tea Shop Locations 🧋🧼

## Business Problem 💼
The bubble tea shop dataset contains dirty location and ratings data that must be cleaned before it can be reliably used to analyze store performance and customer satisfaction.

## Dataset 📊
- Source: Google Data Analytics – Process Data from Dirty to Clean, Hands-On Activity: Clean data with spreadsheet functions.  
- Data type: Store locations, Yelp ratings, and related attributes for a bubble tea shop chain.

## Tools 🛠️
- Google Sheets (or Excel)
- Built-in data cleaning features: Remove duplicates, filters, Split text to columns
- Spreadsheet formulas (e.g., UNIQUE, SPLIT, IF/OR)

## Steps ✅

1. **Import**
   - Import the original CSV into Google Sheets.
   - Save a copy as `boba_tea_raw` and another as `boba_tea_cleaned`.

2. **Initial Data Review 👀**
   - Scroll through the raw sheet to identify obvious issues: duplicates, strange ratings, combined columns, missing values.

3. **Remove Duplicates 🔁**
   - Use `Data → Remove duplicates` on the full table or key columns (e.g., store ID + address).
   - Optionally apply `=UNIQUE(range)` to create a de-duplicated list.

4. **Validate Rating Ranges ⭐**
   - Define a valid rating range (0 to 5 for Yelp ratings).
   - Add a helper column with a formula like `=OR(Rating<0, Rating>5)` to flag invalid entries.
   - Correct or remove rows with invalid ratings.

5. **Fix Column Structure (Latitude/Longitude) 🌍**
   - Identify combined columns like `"latitude,longitude"`.
   - Use `Split text to columns` or `=SPLIT(lat_long_cell, ",")` to create separate Latitude and Longitude columns.
   - Convert them to numeric format if needed.

6. **Final Data Quality Checks ✅**
   - Check for remaining blanks in key fields (store ID, address, rating).
   - Confirm row counts and unique store counts after cleaning.
   - Ensure column types (number, text, date) are appropriate.

## Visuals 🖼️

_Add screenshots (PNG) showing:_
- Raw data with issues (duplicates, odd ratings, combined lat/long)
- Cleaned data after each major step (duplicates removed, ratings fixed, lat/long split)

Example:

- `images/raw_data_issues.png`
- `images/duplicates_removed.png`
- `images/lat_long_split.png`

## Insights 💡

- Removing duplicate rows keeps store counts and performance metrics accurate and not inflated by repeated records.  
- Validating ratings within an accepted range prevents misleading averages and store comparisons.  
- Splitting latitude and longitude into separate numeric columns enables mapping, distance calculations, and spatial analysis.

## Files in This Repository 📁

- `boba_tea_raw.csv` – Original, uncleaned dataset (or as close as license allows)
- `boba_tea_cleaned.csv` – Cleaned dataset ready for analysis
- `cleaning_steps.md` – Short description of manual cleaning steps (optional)
- `images/` – Screenshots showing before/after cleaning

## How This Demonstrates Data Analyst Skills 📈

- Practical data cleaning in spreadsheets on a real-world style dataset.
- Identification and correction of duplicates, out-of-range values, and structural issues.
- Preparation of high-quality data that can feed into further analysis, dashboards, or models.
