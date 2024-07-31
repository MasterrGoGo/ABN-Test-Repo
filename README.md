Pipeline
This repository contains code and instructions for implementing a data pipeline that ingests data from various sources, processes it, and calculates collateral status based on market values.
Problem Statement
We have the following data sources:
•	stocks.json: Real-time stock market information containing stock prices for different assets.
•	Clients.csv: Data about clients.
•	Collaterals.csv: Collateral credit information for some clients, including stock assets.
Solution Components
1.	Ingestion:
o	Use Azure Data Factory (ADF) to ingest the data files into Azure Databricks.
o	Normalize the JSON data from stocks.json into a structured format.
o	Load Clients.csv and Collaterals.csv into DataFrames.
2.	Data Processing:
o	Join the data from Clients.csv and Collaterals.csv to get relevant information.
o	Calculate the market value of each collateral based on stock prices.
o	Determine the fluctuation in collateral value over time.
3.	Collateral Status Table:
o	Create a target table called collateral_status.
o	Include columns: client_id, collateral_id, and fluctuation.
o	Save the resulting table to an appropriate storage location.
Implementation
1.	Databricks Notebooks:
o	Create Databricks notebooks for each step (ingestion, processing, and table creation).
o	Use Python or Scala for data processing.
o	Pass parameters from ADF to notebooks.
2.	Unit Tests:
o	Write unit tests for each function or logic block.
o	Test JSON ingestion, join operation, fluctuation calculation, and table saving.
3.	README.md:
o	Document the steps to set up the pipeline.
o	Explain how to run the notebooks.
o	Provide any necessary configuration details.
Usage
1.	Set up your Azure Databricks workspace.
2.	Create an ADF pipeline to trigger the notebooks.
3.	Execute the notebooks in the specified order.
4.	Verify the collateral status table in your chosen storage location.

