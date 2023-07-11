
# Explore Analytical Data Processing 

Analytical Data Processing:
> Read-only / read-mostly systems stores vast volumes of historical data or business metrics.

Analytical are based on a snapshot of data at a given time.

**Common analytics architecture:**

1. Data files stored in a central data lake for analysis
2. Extract, transfer, load process copies data from files and databases into a data warehouse which is
   relational database that is optimised for read activity. Schema is based on fact tables that 
   contain numeric values to analyse with related dimension tables that represent entities by which 
   you want to measure them
3. Data warehouse may be loaded into an online analytical processing model (OLAP)
4. Data is queried to produce reports

OLAP:
> Aggregated data storage optimised for analytical workloads. Aggreations are across dimensions at
> different levels. This allows easy querying by several factors, e.g: region, by city, by addresses.

