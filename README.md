# Sea Around Us

## Project Overview

The [Sea Around Us](http://www.seaaroundus.org/) is an international research initiative at the University of British Columbia, which acts as a critical resource to assess the impact of fisheries on marine environments. The Sea Around Us seeks to improve data access to enhance the meaningful analysis and research through the website and broaden the impact of this important dataset.

To improve data access for researchers requesting large datasets, results of certain queries from the SAU database are exposed in Amazon S3 and are accessible through Jupyter notebooks. This enables power users to do more in depth analysis on the SAU dataset and also visualize results as needed. The proposed solution involves AWS services such as RDS, Glue, Athena, and S3 to generate a subset of SAU data for further analysis. This is done only once or twice a year or when there is a change in data. On a day-to-day basis, this subset of data in S3 is loaded into Jupyter notebooks for further analysis and visualizations. This enables power users and analysts to perform data analysis or create custom visualizations as needed within the notebook itself instead of relying on the SAU website.

As seen in the architecture diagram below, the first part of the workflow involves exporting the snapshot of the Sea Around Us PostgreSQL database (filtered to only the necessary tables) to S3. Then the metadata of this data is captured with the help of Glue crawlers. The data in S3 is now ready to be queried from Athena in a server-less fashion. When the queries are run on Athena, CSV files are automatically generated in relevant folders on S3. This is the subset of SAU data highlighted in the diagram below, and the subset of data includes aggregated results from SQL queries for example. In the second part of the workflow (the day-to-day scenario), an analyst or a power user can load this subset of SAU data into Jupyter notebooks in any environment for further analysis and visualizations - generating insights from data.

## High level Architecture Diagram

![Architecture diagram](images/Architecture_Diagram.png)



## User Guides

Documentation for different steps involved in this project is added in individual user guides in the `docs` folder of this repository.

## Deployment Guide

The instructions provided in this repository refer to several tools and libraries for conducting data analysis and creating visualizations. This is a brief overview of the installations for these tools and libraries, please refer to official documentation for in-depth details.

**Python** : Head over to `https://www.python.org/` and navigate to specific `Downloads` section for instructions based on your operating system. Download the latest stable release of Python for your computer and operating system. Verify the successful installation by entering `python` in the command window terminal - a response from python interpreter should be received including it's version number.

**Jupyter Notebook** : The Jupyter notebook environment helps in analyzing the SAU data present in the S3 public bucket of SAU. Navigate to `Getting started with the classic Jupyter Notebook` section in the official Jupyter website `https://jupyter.org/install`. and install Jupyter Notebook as per the given instructions. If you are not already familiar with usage of Jupyter, refer to `https://jupyter.readthedocs.io/en/latest/running.html#running` for further details on how to run Jupyter Notebooks.

**Anaconda** : Instead of installing above tools individually, a popular alternative is to use open source Anaconda Individual Edition distribution that includes Python, R, necessary tools like Jupyter Notebooks, and commonly used packages such as Pandas and NumPy by default as part of it's installation. Refer to `https://www.anaconda.com/products/individual` for further details.

**Additional Packages** : Additional packages necessary for data analysis and visualizations can be installed by referring to the install instructions from official sources. For example, `pandas` library for python can be installed using either `conda install pandas` or `pip install pandas` command as mentioned in `https://pypi.org/project/pandas/`. These packages can also be installed from within the notebooks as highlighted on top in the example notebooks. 

## Example Notebooks

Jupyter notebooks that demonstrate different scenarios related to data analysis, visualizations, and data access are included in the `notebooks` folder of this repository.

## License

This project is distributed under [MIT License](https://github.com/UBC-CIC/Sea-Around-Us/blob/main/LICENSE).

