# Home_Sales
Home_Sales
 Home Sales Data Analysis with PySpark
This project demonstrates how to use Apache Spark within a Google Colab environment to analyze a real estate dataset. The dataset includes various home sales data points such as price, number of bedrooms, bathrooms, square footage, and more.

The analysis focuses on querying the data using Spark SQL, performance optimization using caching and parquet partitioning, and comparing query runtimes across different storage strategies.

 Key Tasks Performed
 Environment Setup
Installed Apache Spark 3.5.5 and Java 11
Configured environment variables for Spark and Java
Initialized Spark session using findspark in Google Colab
 Data Loading
Loaded home_sales_revised.csv from an AWS S3 bucket
Created a temporary view home_sales for SQL querying
 Data Analysis with Spark SQL
Average Price of 4-Bedroom Homes per Year

Grouped by sale year
Calculated and rounded the average sale price
Average Price by Year Built for 3-Bed, 3-Bath Homes

Grouped by date_built
Filtered for homes with 3 bedrooms and 3 bathrooms
Average Price for 3-Bed, 3-Bath, 2-Story Homes ≥ 2000 sqft

Grouped by date_built
Applied multiple filters and calculated average price
Average Price per View Rating (Only Views ≥ $350K Avg Price)

Grouped by view rating
Ordered by descending view score
Timed for performance benchmarking
 Performance Optimization
 Caching
Cached the home_sales temporary view to speed up repeated queries
Measured and compared runtime before and after caching
 Partitioning with Parquet
Wrote data into Parquet format, partitioned by date_built
Created a new temporary view parquet_home_sales
Re-ran the same query to compare runtime using Parquet partitioning
 Uncaching
Uncached the home_sales table after testing
 How to Use This Notebook
Open the notebook in Google Colab
Run all cells in order
Modify SQL queries or filters to explore the dataset further
Observe runtime improvements using cache and parquet partitions
 Requirements
Python 3.x (runs in Colab)
Google Colab with internet access
No local installation needed
 Skills & Concepts Practiced
Spark SQL querying
Performance tuning with caching
Partitioning large datasets using Parquet
Measuring execution time for Spark operations
Data analysis and transformation with PySpark

