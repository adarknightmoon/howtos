# How to Create Interactive SQL Filters in Metabase?

**Question:** 
How can I allow users to dynamically filter data on a Metabase dashboard when using a custom SQL query?

**Answer:**
To make your custom SQL queries interactive in Metabase, you need to use **Field Filters** (SQL variables). 

1. Write your SQL query and enclose the variable in double curly braces, like this: `{{variable_name}}`.
   *Example:* `SELECT * FROM users WHERE {{created_at}}`
2. A side panel will appear in the Metabase editor. Set the **Variable Type** to "Field Filter".
3. Map this variable to the corresponding database column (e.g., `Users -> Created At`).
4. Save the question and add it to a dashboard.
5. Add a filter to the dashboard and link it to the variable you just created. The dashboard filter will now dynamically update your SQL results.
