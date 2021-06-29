## Why?

Typically, data is extracted from databases for analysis. But in a server-less architecture, a database server is not required for analysis. For example, as discussed earlier, a database snapshot can be exported to S3, and Glue crawlers can be setup to extract the metadata or the structure of this data. This data can be then accessed via Athena (or) directly in SageMaker notebooks. This allows us to extract the necessary data, and conduct data analysis or create visualizations on top of this data – everything from within the notebook.



## How?

Data in S3 can be accessed in multiple ways –      

* Using parquet files in S3 from Athena      
* Using CSV files present in S3        

### Using Athena

If the data is in the form of a compressed parquet file and Glue crawlers are already setup for this data, then SQL queries can be written directly in notebooks via AWS Athena. Python library called PyAthena can be used to make this connection – PyAthena is an API client for AWS Athena. Please refer to sample notebooks provided in this repository for further details and examples.

### Using S3 data directly in notebooks

If the data is in the form of a CSV file in S3, then this data can be directly accessed in notebooks via Pandas library in Python. Please refer to sample notebooks provided in this repository for further details and examples.

