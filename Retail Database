-- =================================================================================================
-- Problem 1: Database Record Count
-- Business Question:
-- How many customers, orders, order-detail records, products, and categories are stored
-- in the database?
--
-- Goal:
-- Count the number of records in each of the five main tables and combine the results
-- into a single result set.
-- =================================================================================================


-- Step 1: Count the number of records in the customers table.

SELECT 
    'customers' AS table_name,       -- 'customers' is a text value, not a column name.
                                     -- AS table_name gives this output column a descriptive alias.

    COUNT(*) AS total_records         -- COUNT(*) counts every row in the customers table.
                                     -- AS total_records gives the calculated result a readable name.

FROM customers                        -- Specifies the table from which the rows are counted.


-- At this point, the query above would return one row similar to:
--
-- table_name     total_records
-- customers      1000
--
-- The same type of query could be written separately for each table. However, running
-- separate SELECT statements would produce separate result sets.
--
-- UNION ALL allows the results of each SELECT statement to be combined vertically
-- into one result set.


UNION ALL                             -- Combines this result with the result of the next SELECT.
                                      -- UNION ALL keeps every returned row.
                                      --
                                      -- UNION could also combine the queries, but UNION removes
                                      -- duplicate rows. Because duplicate removal is unnecessary
                                      -- for this analysis, UNION ALL is the more appropriate choice.


-- Step 2: Repeat the same process for the remaining tables.

SELECT 
    'orders' AS table_name,
    COUNT(*) AS total_records
FROM orders


UNION ALL


SELECT 
    'catagories' AS table_name,       -- "catagories" matches the table name used in this database.
    COUNT(*) AS total_records
FROM catagories


UNION ALL


SELECT 
    'order_details' AS table_name,
    COUNT(*) AS total_records
FROM order_details


UNION ALL


SELECT 
    'products' AS table_name,
    COUNT(*) AS total_records
FROM products;


-- Final Result:
-- The query returns five rows in one result set, with each row showing the total
-- number of records contained in one of the database's main tables.
--
-- Example structure:
--
-- table_name       total_records
-- --------------------------------
-- customers        ...
-- orders           ...
-- catagories       ...
-- order_details    ...
-- products         ...
--
-- Key SQL concepts demonstrated:
-- COUNT(*)  = Counts all rows in a table.
-- AS        = Assigns a temporary, readable name (alias) to an output column.
-- UNION ALL = Combines rows returned by multiple SELECT statements into one result set.
-- =================================================================================================
