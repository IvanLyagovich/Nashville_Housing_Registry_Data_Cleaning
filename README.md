## README for the SQL File

This SQL file contains a series of queries and operations performed on the "NashvilleHousing" table within the "PortfolioProject.dbo" database. The purpose of these queries is to standardize and transform data within the table. Here is a brief overview of each section:

1. **Standardize Date Format:**
   - Converts the "SaleDate" column to a standardized date format using the CONVERT function.

2. **Populate Property Address data:**
   - Populates missing values in the "PropertyAddress" column by joining records with the same "ParcelID" but different "UniqueID" and updating the null values.

3. **Breaking out Address into Individual Columns (Address, City, State):**
   - Splits the "PropertyAddress" column into separate columns for "Address" and "City" by using the SUBSTRING function and the CHARINDEX function.

4. **Breaking out Owner Address into Individual Columns (Address, City, State):**
   - Splits the "OwnerAddress" column into separate columns for "Address," "City," and "State" by using the PARSENAME function and replacing commas with periods.

5. **Change Y and N to Yes and No in "Sold as Vacant" field:**
   - Updates the values in the "SoldAsVacant" column from "Y" to "Yes" and from "N" to "No" using a CASE statement.

6. **Remove Duplicates:**
   - Removes duplicate records from the table based on the combination of "ParcelID," "PropertyAddress," "SalePrice," "SaleDate," and "LegalReference" columns, keeping only the first occurrence.

7. **Delete Unused Columns:**
   - Removes the "OwnerAddress," "TaxDistrict," "PropertyAddress," and "SaleDate" columns from the table.

Please note that these queries assume the existence of the "NashvilleHousing" table in the "PortfolioProject.dbo" database. Before executing these queries, ensure that you have the necessary permissions and have made any required modifications based on your specific database schema.
