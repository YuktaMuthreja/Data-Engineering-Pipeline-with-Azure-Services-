## Data-Engineering-Pipeline-with-Azure-Services-

## Project Summary: Data Pipeline Migration to Azure

This project demonstrates a comprehensive data pipeline designed within Azure to migrate data from an on-premise SQL Server database to the Azure cloud. The pipeline encompasses several key stages: data extraction, transformation, loading, and analytics, culminating in dynamic visualizations through Power BI dashboards.

![image](https://github.com/YuktaMuthreja/Data-Engineering-Pipeline-with-Azure-Services-/assets/145282953/9c65ef34-f9d2-4ba9-9c3c-60efffa716df)



## Key Components:

### ADF Pipeline for Data Extraction:
Utilizes Azure Data Factory (ADF) to connect to the on-premise SQL Server database.
Selected tables are extracted and loaded into Azure Data Lake Storage Gen2 (ADLS Gen2), initially stored in the "Bronze" container.

### Azure Databricks for Data Transformation:
Azure Databricks is employed to transform data stored in the "Bronze" container, applying various transformations to prepare it for analytics.
Transformed data is then deposited into both the "Silver" and "Gold" containers within ADLS Gen2.

### Azure Synapse Analytics for Data Analytics:
Azure Synapse Analytics conducts advanced analytics on the migrated data.
A database is established in Azure SQL Server within Synapse Analytics.
Views are generated within the database using an Azure Synapse Pipeline, which leverages ADLS locations to identify table names and generate views.
A stored procedure automates the view creation process, with parameters passed through the Synapse Pipeline.

### Power BI for Dashboarding:
The views created in Azure Synapse Analytics are connected to Power BI.
Power BI facilitates the creation of dynamic, interactive dashboards to visualize and analyze the data.
