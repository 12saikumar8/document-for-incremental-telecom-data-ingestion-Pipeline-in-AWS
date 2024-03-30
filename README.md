# document-for-incremental-telecom-data-ingestion-Pipeline-in-AWS
The data pipeline is structured around an S3 data lake serving as the primary repository, where it regularly receives daily CSV files from an upstream client. These files are systematically organized within the S3 bucket, segmented into partitions by date, denoted as date=2023-08-21, date=2023-08-22, and so on.

The ultimate objective is to feed data into an RDS database optimized for telecom operations, housing a 'sales' database and a 'customer_subscription' table. Glue acts as a pivotal component within the pipeline, facilitating seamless data transfer and management between the source (S3) and the destination (RDS).

In the ETL process, Glue diligently sifts through records, specifically targeting those associated with prepaid customers. This ensures that only relevant data is channeled into the RDS target. Moreover, the pipeline operates in an incremental manner, efficiently processing each daily CSV file received from the data lake and integrating the updates into the target table within the RDS database.

AWS services used in this project are S3, RDS,GLUE,IAM, and In Glue (Crawlers,Connectors, Database, Etl jobs,Visual ETL).
