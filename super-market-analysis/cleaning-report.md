**Data Cleaning Report**

**1. Problems in Data**
- Presence of missing values in multiple columns.
- Duplicate rows that could distort analysis.
- Inconsistent data structure with redundant columns.
- Incorrect data types, particularly in the `Date` column.
- Erroneous or inconsistent values in categorical and numerical columns.

**2. Handling Missing Values**
- Identified missing values using `df.isnull().sum()`.
- Removed rows containing missing values using `df.dropna(inplace=True)`.

**3. Handling Duplicates**
- Checked for duplicate rows using `df.duplicated().sum()`.
- Removed duplicate rows using `df.drop_duplicates(inplace=True)`.

**4. Fixing Column Structure**
- Combined three columns (`Yangon`, `Naypyitaw`, `Mandalay`) into a new `Location` column using `idxmax()`.
- Dropped the original columns after merging to reduce redundancy.

**5. Data Type Conversion**
- Converted the `Date` column to datetime format using `pd.to_datetime(df['Date'])`.

**6. Handling Incorrect Values**
- Standardized values in the `Customer type` column:
  - Replaced incorrect entries: "Memberr" → "Member" and "-" → "Member".
- Fixed a rating error: replaced `97` with `9.7` to correct a typo.

**Summary**
- The dataset was successfully cleaned by removing missing values and duplicates, restructuring columns, converting data types, and fixing incorrect values.
- The cleaned dataset is now ready for further analysis.

