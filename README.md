# Nashville Housing Data Cleaning Project

## Project Overview
This project involves cleaning and transforming raw Nashville housing data using SQL queries. The goal is to standardize, split, and clean the data to make it more usable for analysis, while also handling issues like missing data, duplicates, and formatting inconsistencies.

## Key Features
1. **Date Standardization**:
   - Converted the `SaleDate` column to a standardized `Date` format.
   - Handled potential issues with updating by adding a new `SaleDateConverted` column.

2. **Populating Missing Property Addresses**:
   - Used SQL joins to populate missing `PropertyAddress` values by matching records based on `ParcelID` where the address was null.

3. **Splitting Address Columns**:
   - Separated the `PropertyAddress` and `OwnerAddress` into individual components (Address, City, State) using string manipulation functions like `SUBSTRING` and `PARSENAME`.

4. **Data Transformation**:
   - Changed the `SoldAsVacant` field values from 'Y' and 'N' to 'Yes' and 'No' for consistency and readability.

5. **Removing Duplicates**:
   - Applied a Common Table Expression (CTE) to identify and remove duplicate records based on key fields like `ParcelID`, `PropertyAddress`, `SalePrice`, and `SaleDate`.

6. **Dropping Unused Columns**:
   - Removed unused or redundant columns, such as `OwnerAddress`, `TaxDistrict`, `PropertyAddress`, and `SaleDate`, to streamline the dataset.

## Tech Stack
- **SQL Server**
- **SQL Queries**: Data transformation, string manipulation, CTEs, JOINs

## Business Impact
This project provides a clean and standardized dataset for further analysis, improving the usability of Nashville housing data. The cleaned data can be used for property market analysis, sales forecasting, and other real estate-related insights.

## Acknowledgments
Special thanks to the creators of the Nashville Housing dataset for providing the raw data for this project.
