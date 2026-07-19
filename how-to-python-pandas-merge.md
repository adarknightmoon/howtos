# How to Join Multiple Datasets in Python?

**Question:** 
How do I combine two separate datasets (DataFrames) based on a common key or column using Python and Pandas?

**Answer:**
You can combine DataFrames using the **`pd.merge()`** function, which works similarly to SQL JOINs.

1. First, import pandas and load your datasets:
```python
   import pandas as pd
   df_users = pd.read_csv('users.csv') # Contains 'user_id' and 'name'
   df_sales = pd.read_csv('sales.csv') # Contains 'user_id' and 'amount'
   
