## Why?

Once initial data analysis is completed or visualizations are created in a Jupyter notebook, users might want to download the data behind those tables and charts for future reference or for further exploration and analysis.



## How?

There are several ways to download data from a Jupyter notebook. Easiest way for notebook users to export the Pandas data frame to csv using to_csv function `df.to_csv('file1.csv')`. But if the notebook is not being run on user’s local environment – then it might add some complexity around fetching files from the server where the notebook would save the CSV file.      

Another approach is to leverage Java Script to run the download application on client side. This approach allows the user to fetch the data similar to a download from a website. Please refer to examples in notebooks section of this repository for more details about this download data functionality.

