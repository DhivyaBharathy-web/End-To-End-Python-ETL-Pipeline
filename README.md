# End-To-End-Python-ETL-Pipeline
Extract Data from Zillow Rapid API:

Used Python to connect to the Zillow Rapid API.
Extracted the data needed from Zillow.
Load Data into S3 (Landing Zone):

Loaded the extracted data into an Amazon S3 bucket, which acts as the landing zone.
Trigger First Lambda Function:

A Lambda function is triggered by the data upload in the landing zone S3 bucket.
This function copies the data from the landing zone to an intermediate zone in another S3 bucket.
Trigger Second Lambda Function:

The data in the intermediate zone S3 bucket triggers another Lambda function.
This function transforms the data according to your requirements.
Load Transformed Data into S3 and Redshift:

The transformed data is then loaded into a separate S3 bucket (transformed data).
Finally, the data is loaded into Amazon Redshift for further processing and analysis.
Visualize Data using QuickSight:

Connected the data in Redshift to Amazon QuickSight for visualization.
Orchestrate the Process with Apache Airflow:

Set up Apache Airflow on an Amazon EC2 instance to orchestrate and manage the entire pipeline.
