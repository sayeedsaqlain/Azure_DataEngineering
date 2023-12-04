# Azure_DataEngineering

Hi, In this project, I have built an end 2 end data engineering pipeline on Azure data platform.
I have utilized tools such as Azure Data Factory(ADF), Data Lake Storage Gen2(ADLS), Azure Databricks, Synapse Analytics in setting up an ETL data pipeline for data ingestion, transformation, loading and analytics.

For this project, I am using the Tokyo Olympics dataset from Kaggle. I will be integrating the dataset from github to Data factory, then loading it into Data Lake. Further, setting up Databricks instance to write spark code to fetch this data
and perform transformations to loading it back to Data Lake Container. For Analytics, we will link the transformed data to Synapse Analytics to write SQL queries for analysis.

### Architecture
1. WorkFlow
  
2. Resource Group overview
  <img width="960" alt="image" src="https://github.com/sayeedsaqlain/Azure_DataEngineering/assets/41228969/1b06fd6f-7467-4f97-8166-ad79edc8f5f2">


### Azure Data Factory (ADF)
I have authored a new pipeline to link source data from HTTP webpage (such as github repo) to ADF and sink it into Data Lake storage as raw data format.

<img width="960" alt="image" src="https://github.com/sayeedsaqlain/Azure_DataEngineering/assets/41228969/22f85948-2510-4b04-809c-7d8cce09d8c4">

### Azure Data Lake Storage Gen2 (ADLS)
I have created a raw-data folder hosting the newly ingested data files from Data Factory into the data lake container.

<img width="960" alt="image" src="https://github.com/sayeedsaqlain/Azure_DataEngineering/assets/41228969/057c2fe2-59d9-4e48-b772-d799299a60a4">

### Azure Databricks
With the help of Apache spark, we can create a connection to fetch data from Data Lake storage, perform data cleaning/transformation steps using PySpark and write updated file version back to Data lake container under transformed-data folder.

Create connection

<img width="960" alt="image" src="https://github.com/sayeedsaqlain/Azure_DataEngineering/assets/41228969/64cbe748-d6b0-43d9-8d94-e68fa3895348">

Transformation

<img width="960" alt="image" src="https://github.com/sayeedsaqlain/Azure_DataEngineering/assets/41228969/d4d720a8-821a-4a62-8707-6386cf8527ef">

Write back

<img width="746" alt="image" src="https://github.com/sayeedsaqlain/Azure_DataEngineering/assets/41228969/c6886659-041d-4e88-8290-b087a461234e">

### Synapse Analytics
Leveraging Synapse studio, we can create tables from data lake files to run SQL analysis and quick visual charts.

<img width="730" alt="image" src="https://github.com/sayeedsaqlain/Azure_DataEngineering/assets/41228969/5aa1d126-10f3-47d1-b63b-3062c4f4bfd9">

<img width="957" alt="image" src="https://github.com/sayeedsaqlain/Azure_DataEngineering/assets/41228969/c1b74ff6-e73b-4fcb-a241-963551782bed">










