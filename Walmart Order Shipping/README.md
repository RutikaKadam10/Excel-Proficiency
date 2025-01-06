Business Case: Walmart Order Shipping

Scenario
You are an analyst of Walmart and trying to understand some order patterns in the data. For that, you have a Dataset workbook where details of the orders are written at
the order_id and product_id levels. For example, if a customer is placing an order (CA-2013-101672) having 3 products (OFF-PA-10004610, FUR-CH-10004063, OFF-LA-10002271), 
then the dataset would have 3 rows for the given order. Hence, in the table, you might find duplicate order_id. However, the combination of order_id and product_id would be unique.<br>
An example is also written in Table 1

Table 1: Example of order_id and product_id<br>
order_id product_id Other columns Other columns …<br>
CA-2013-101672 OFF-PA-10004610 … … …<br>
CA-2013-101672 FUR-CH-10004063 … … …<br>
CA-2013-101672 OFF-LA-10002271 … … …<br>

Product id is made up of 3 codes:<br>
Category code: First 3 characters code (example: OFF, FUR)<br>
Sub-category code: 2 characters code in the middle (example: PA, CH, LA)<br>
Item_code: 8 digit code in the last (example: 10004610, 10004063, 10002271)<br>

Task is to fill the blank columns of the sheet.

In this assignment to fill the blanks columns in 'Data' sheet we use 'Mapping' sheet in 'Walmart Order Shipping' Workbook : 
1. We separate first three alphabets of 'Product Id' column, which represent Category code and store it in column named 'Column1' - we use function =left(), which is later required to fill 'Category' column.
2. We separate middle two alphabets which represent Sub-Category code and store it in column named 'Column3' - we use function =mid(), which is later used to fill 'Sub-category' column.
3. To fill columns like 'Order Date', 'Ship Date', 'Postal Code', 'City', 'State', 'Country', 'Region', 'Category','Sub-category' =vlookup() function in excel is used.
4. To fill columns like 'Ship Mode','Segment' index-match function is used.
