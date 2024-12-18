# Power BI Test Task

## Implementation Details

### 1. Handling Missing Product Types
- I didn't hide the missing product type (Type 7) in the matrix. This could provide valuable insights into gaps or anomalies in the data.

### 2. Combining and Cleaning Sales Data
- Two sales files were appended in Power Query, with one of them disabled from loading into the report.
- Cleaned the price column by removing non-numeric characters  "EUR".

### 3. Fixing and Formatting Dates
- Corrected date formats.
- Split datetime fields into separate date and time columns.

### 4. Calendar Table and Dual-Date Plot
- Created a calendar table and connected it to both transaction and departure dates.
- Used the `USERELATIONSHIP` function to work with inactive relationships, because RLS is not used here.

### 5. Dynamic Country Chart
- Developed a dynamic chart for countries with parameters for interactivity and dynamically updating chart titles.

### 6. Preventing Incorrect Percentages
- Used `ISINSCOPE` to avoid displaying unnecessary 100% values for each product category in the matrix.

### 7. Date Filters with Hierarchy
- Added two date filters: one for transaction dates and another for departure dates.
- Created an additional calendar table specifically for filters to include a date hierarchy. This improvement, although optional, but the date hierarchy is the most convenient type of filters for me.

Screenshot of the main page:
![image](https://github.com/user-attachments/assets/9d292979-f7c6-47a1-809a-589d47ec80e3)
