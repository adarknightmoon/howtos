# How to Perform SQL-like Data Aggregation in Google Sheets?

**Question:** 
How can I efficiently filter, sort, and aggregate a large raw dataset in Google Sheets without using complex pivot tables or multiple VLOOKUPs?

**Answer:**
You can use the built-in **`QUERY`** function, which allows you to write SQL-like commands directly inside a cell.

1. Select an empty cell where you want the processed data to appear.
2. Use the syntax: `=QUERY(data_range, "query_string", [headers])`
3. *Example:* If your raw data is in `A1:D1000` (where column A is 'Department' and column C is 'Salary'), and you want to find the average salary per department for those earning over $50,000:
   `=QUERY(A1:D1000, "SELECT A, AVG(C) WHERE C > 50000 GROUP BY A", 1)`
4. The function will dynamically output a clean, aggregated table that updates automatically as your raw data changes.
