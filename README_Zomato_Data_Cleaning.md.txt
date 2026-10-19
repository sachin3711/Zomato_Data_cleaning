# Zomato Data Cleaning & Preparation (Microsoft Excel)

## 1. Project Overview
This project focuses on preparing Zomato restaurant and menu data for reliable analysis using Microsoft Excel. The work compares the original dataset with a cleaned version and documents visible data-quality improvements and remaining validation needs.

The objective of data cleaning is to improve consistency, reduce avoidable data-quality issues, and make the dataset easier to filter, summarize, and use in reports or dashboards.

## 2. Dataset Information
Two Excel workbooks were compared:
- **Raw dataset:** `zomato_row_Dataset.xlsx`
- **Cleaned dataset:** `zomato_clean_Dataset.xlsx`

The dataset contains restaurant/menu-related fields such as `State`, `City`, `Order Date`, `Day wise`, `Restaurant Name`, `Location`, `Category`, `Dish Name`, `Food Type`, `Price (INR)`, `Rating`, and `Total Review`.

The cleaned workbook includes the additional `Day wise` and `Food Type` fields. The original source URL and extraction date were not available in the workbook information; add them if known.

## 3. Data Quality Checks
The raw and cleaned workbooks were compared for:
- Completely blank rows and missing values
- Exact duplicate rows
- Leading/trailing spaces in text fields
- Text capitalization consistency
- Date and numeric data types
- Changes to review-count values
- Missing values in derived fields

## 4. Cleaning and Preparation Work
The following changes are visible when comparing the supplied workbooks:

1. **Blank rows:** The raw workbook contained fully blank rows; the cleaned workbook does not contain fully blank rows.
2. **Additional fields:** `Day wise` and `Food Type` appear in the cleaned workbook.
3. **Text formatting:** Leading/trailing spaces are no longer detected in `Dish Name`. Some capitalization has also been standardized in text fields.
4. **Numeric formatting:** `Total Review` is stored as an integer in the cleaned workbook.
5. **Validation needs:** Duplicate rows, spacing issues in `Location` and `Category`, and missing `Day wise` values remain.
6. **Review-count change:** The raw workbook contained zero values in `Total Review`, while the cleaned workbook contains positive values only. The rule used for this change needs to be confirmed before the dataset is used for analysis.

This README describes changes visible in the output files. It does not claim that a particular Excel formula or command was used unless that method has been confirmed by the person who performed the cleaning.

## 5. Before-and-After Summary

| Check | Raw dataset | Cleaned dataset / observation |
|---|---|---|
| Worksheet | `Sheet1` | `Sheet1` |
| Columns | 10 | 12 |
| Rows read from worksheet | 152,741 | 152,740 |
| Fully blank rows | 3 | 0 |
| Missing cells | 30 | 2, both in `Day wise` |
| Exact duplicate rows detected | 26, including blank-row duplicates | 27 |
| `Dish Name` leading/trailing spaces | Detected | Not detected |
| `Location` leading/trailing spaces | Detected in 394 cells | Still detected in 394 cells |
| `Category` leading/trailing spaces | Detected in 914 cells | Still detected in 914 cells |
| `Total Review` | Contains zero values | Stored as integer; no zero values remain |

*Counts are based on the supplied workbook comparison. Exact duplicate counts depend on the columns and values included in the comparison.*

## 6. Validation Notes
Before using this dataset for analysis or a dashboard, review these items:

- **Duplicate records:** Exact duplicate rows are still detected in the cleaned workbook. Confirm whether they are accidental duplicates or valid repeated observations.
- **Text spacing:** Leading/trailing spaces remain in `Location` and `Category`. These can affect grouping and filtering.
- **Missing `Day wise`:** Two values are missing. If `Day wise` is derived from `Order Date`, validate the date-to-day formula and fill only after confirming the correct rule.
- **`Total Review` values:** Confirm why raw zero values became positive values. Do not use the changed review counts for analysis until the transformation rule is understood.
- **`Food Type`:** Confirm the rules used to classify records as `Veg` or `Non Veg`.
- **Source and date meaning:** Add the original dataset URL and clarify what `Order Date` represents if that information is available.

## 7. Tools
- Microsoft Excel
- Worksheet comparison and data-quality checks

Specific Excel features or formulas should be listed as methods used only if they were actually applied during the project.

## 8. Outcome
The cleaned workbook has two additional fields, no fully blank rows, and no detected leading/trailing spaces in `Dish Name`. It is more structured for further review, but it still needs validation for duplicate records, spacing in `Location` and `Category`, missing `Day wise` values, and the change in `Total Review`.

After these checks are resolved, the dataset could be used for restaurant/location comparisons, menu-category summaries, price and rating analysis, and a future Power BI dashboard.

## 9. Limitations
- The original dataset source URL and extraction date were not provided.
- The exact Excel commands or formulas used cannot be established from the workbook outputs alone.
- The business meaning and derivation rules for `Order Date`, `Day wise`, `Food Type`, and `Total Review` should be confirmed.
- No claims about restaurant performance are made in this project README.

## 10. Conclusion
This project documents a Microsoft Excel-based data cleaning and preparation workflow for Zomato restaurant/menu data. It highlights observable changes between the raw and cleaned workbooks and identifies remaining issues that should be validated before analysis. Recording these checks makes the cleaning process more transparent and helps avoid unsupported conclusions.
