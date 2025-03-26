# Spotify ETL Pipeline Project with AWS

### Description
Built an end-to-end ETL (Extract Transform, Load) Pipeline using Spotify API on AWS. Data is retrieved from the Spotify API, transformed into the desired format, and is loaded into an AWS data storage bucket which is then used in AWS Athena to perform analytical functions on the same.

### Architecture

![Architecture Diagram](https://github.com/Prithvijuloori/spotify-etl-pipeline/blob/main/Spotify%20Data%20Pipeline%20Project%20Using%20AWS.png)


### Services Used
1. **S3 (Simple Storage Service):** Amazon S3 (Simple Storage Service) is a cloud storage service that allows users to store and retrieve data from "buckets" (containers) at any time, from anywhere, and on any device, offering scalability, security, and data availability.

2. **AWS Lambda:** AWS Lambda is a serverless compute service from Amazon Web Services (AWS) that lets you run code without provisioning or managing servers, executing code in response to events and automatically handling compute resources.

3. **AWS Cloud Watch:** Amazon CloudWatch is an AWS monitoring service that allows you to collect and track metrics, collect and monitor log files, and set alarms to gain visibility into your AWS resources and applications, enabling you to monitor performance, troubleshoot issues, and optimize resource utilization.

4. **AWS Glue Crawler:** An AWS Glue crawler is an automated service that discovers and catalogs data by scanning various data sources, extracting schema information, and storing metadata in the AWS Glue Data Catalog.

5. **Data Catalog:** The AWS Glue Data Catalog is a centralized, persistent metadata repository that stores information about your data assets, including location, format, schema, and more, enabling efficient data discovery and management across various AWS services, such as Athena.

6. **Amazon Athena:** AWS Athena is a serverless, interactive query service that allows you to analyze data directly in Amazon S3 using standard SQL, without needing to load data into a separate database or manage any infrastructure.


### About the Dataset/API Used
The data is provided by Spotify API which contains information about music artists, albums, and their respective songs - [Spotipy API](https://spotipy.readthedocs.io/en/latest/)

### Python Packages used
```
pip install pandas
pip install numpy
pip install spotipy
```

### Project Execution Flow
Extract Data from API --> Lambda Trigger (every 1 hour) --> Run Extract Code --> Store Raw Data --> Trigger Transform Function --> Transform Data and Load it --> Query Using Athena
