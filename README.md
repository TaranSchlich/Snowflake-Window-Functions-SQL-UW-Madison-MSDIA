# Window Functions  
SQL Analysis Using Snowflake

Applying window functions, aggregation logic, and multi‑step analytical SQL patterns to severe weather event data stored in Snowflake. The assignment required writing SQL, following a style guide, and exporting results into an Excel workbook with separate tabs for each query.

------------------------------------------------------------
Overview
------------------------------------------------------------

The goal of this assignment was to demonstrate proficiency in:

- Window functions (DENSE_RANK, cumulative sums)
- Aggregation and grouping logic
- Time‑based calculations using TIMESTAMPDIFF and EXTRACT
- Multi‑CTE analytical workflows
- Loading external data into Snowflake
- Clean SQL formatting and documentation
- Exporting reproducible results to Excel

All work was executed in Snowflake using the CLASSWORK warehouse and the WEATHER database.

------------------------------------------------------------
Repository Contents
------------------------------------------------------------

GB882_Assignment 5_Window Functions_Schlichtmann_T.txt  
    All SQL statements written for the assignment.

GB883_Assignment 5 - Window Functions_Schlichtmann_T.xlsx  
    Excel workbook containing query results in separate tabs.

README.md  
    Documentation and context for the assignment.

------------------------------------------------------------
Assignment Summary
------------------------------------------------------------

Query 1 — Top 5 Most Common Weather Information Sources  
Identified the five most frequent sources of severe weather reports, ordered by event count.

Result Insight:  
The top source was **Public**.

------------------------------------------------------------

Query 2 — Property Damage Totals by State and Event Type  
Summarized property damage grouped by state and event type, sorted alphabetically.

Result Insight:  
Flash flooding in Alabama caused **14,820,000** in property damage.

------------------------------------------------------------

Query 3 — Longest‑Lasting Weather Event  
Calculated event duration using TIMESTAMPDIFF to determine the longest event in days.

Result Insight:  
The longest event lasted **30 days**.

------------------------------------------------------------

Query 4 — Sequencing Weather Events by County and Storm  
Used DENSE_RANK to sequence storms within each county (cz_type = 'C'), ordered by county and episode sequence.

Result Insight:  
The third storm in Abbeville County, South Carolina had episode ID **162969**.

------------------------------------------------------------

Query 5 — Monthly Damage and Cumulative Damage  
Summarized monthly property damage and computed cumulative totals using a window function.

Result Insight:  
By the end of June, cumulative damage reached **9,986,908,890**.

------------------------------------------------------------

Query 6 — Classifying Sources Using a CASE Statement  
Counted events by source and classified each as a “major source” (> 2,000 events) or “minor source.”

Result Insight:  
**Broadcast media** was identified as a major source.

------------------------------------------------------------

Query 7 — Storms per Square Kilometer (CTE Workflow)  
Built a multi‑CTE pipeline to:

1. Load and convert state land area from square meters to square kilometers  
2. Count storm events by state  
3. Join both datasets and compute storms per square kilometer  

Result Insight:  
The **District of Columbia** had the highest storms‑per‑sq‑km density.

------------------------------------------------------------
Tools & Technologies
------------------------------------------------------------

- Snowflake (SQL execution & data exploration)
- Excel (result storage & reporting)
- SQL Style Guide (formatting & readability standards)

------------------------------------------------------------
Skills Demonstrated
------------------------------------------------------------

- Window functions (DENSE_RANK, cumulative sums)
- Time‑based calculations
- Data loading and staging in Snowflake
- Multi‑CTE analytical design
- Clean, readable SQL following style conventions
- Reproducible result export workflows
