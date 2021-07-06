## Why?

Typically, data is extracted from databases for analysis. But in a server-less architecture, a database server is not required for analysis. For example, as mentioned in the architecture overview, a database snapshot can be exported to S3, and Glue crawlers can be setup to extract the metadata (or) the structure of this data. This data can be then accessed via Athena (or) directly in Jupyter notebooks. This allows us to extract the necessary data, and conduct data analysis or create visualizations on top of this data – everything from within a Jupyter Notebook.

In the case of SAU, a subset of the whole PostgreSQL database can be stored in S3 for further data analysis by power users or analysts. This subset can be either aggregated data, results from SQL queries etc. Providing access to aggregated data or a subset of data for analysis in S3 results in avoiding the queries on the larger database, which saves costs and time.



## How?

Data in S3 can be accessed in multiple ways –      

* Accessing compressed (parquet etc.) files in S3 from Athena      
* Accessing CSV files present in S3 directly        

### Using Athena

If the data is in a compressed format like parquet and Glue crawlers are already setup for this data, then SQL queries can be written directly in notebooks via AWS Athena. Python library called PyAthena can be used to make this connection – PyAthena is an API client for AWS Athena. Please refer to sample notebooks provided in this repository for details and examples that demonstrate basic usage. Refer to `https://pypi.org/project/pyathena/` for additional details and examples related to PyAthena package.

### Using S3 data directly in notebooks

If the data is in the form of a CSV file in S3, then this data can be directly accessed in notebooks via Pandas library in Python. Please refer to sample notebooks provided in this repository for further details and examples that demonstrate basic usage of this functionality.

