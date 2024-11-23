# MarketPulse: Real-Time Data Pipeline with Kafka

## Introduction 
This project is an end-to-end data engineering pipeline built for real-time stock market data using Kafka. The goal is to showcase how to integrate various technologies to manage and process real-time data streams, including handling stock market data from multiple sources.

The project involves real-time data ingestion using Apache Kafka, data transformation using AWS services like Glue, and querying the data using Athena. Python is used for orchestrating the entire pipeline, and the pipeline is designed to run on AWS infrastructure.

## Architecture

![Architecture](Architecture.jpg)

## Technology Stack

- **Programming Language**: Python
- **Cloud Platform**: Amazon Web Services (AWS)
  - **S3** (Simple Storage Service) - for storing processed data.
  - **Athena** - for querying data stored in S3.
  - **Glue Crawler** - for crawling and cataloging data in S3.
  - **Glue Catalog** - for managing metadata.
  - **EC2** - for running the data pipeline components.
- **Data Streaming**: Apache Kafka
  - Used to stream stock market data in real-time.
- **Data Processing**: AWS Glue and Athena

## Dataset

In this project, we focus on building the data pipeline for streaming stock market data. You can use any stock market dataset for this project. The dataset used in the tutorial video can be found at:

[Stock Market Data - indexProcessed.csv](indexProcessed.csv)

## How It Works

1. **Data Ingestion with Kafka**: 
   - Stock market data is streamed into Apache Kafka.
   - Kafka consumers read the data from the topic and push it to AWS services for processing.

2. **Data Processing with AWS Glue**:
   - AWS Glue crawlers are used to create a catalog of the incoming data.
   - The data is processed and stored in S3 for further querying and analysis.

3. **Data Querying with Athena**:
   - The data stored in S3 is queried using Athena to analyze the stock market trends and generate real-time insights.

4. **Data Storage in S3**: 
   - Processed data is saved into S3 buckets for long-term storage and analysis.

## How to Run the Project

1. **Set up AWS Account**: 
   - Ensure you have an AWS account and necessary IAM permissions to access S3, Athena, Glue, and EC2.

2. **Install Kafka**: 
   - Set up Kafka for data streaming.

3. **Run Kafka Producer**: 
   - Use a Kafka producer to stream stock market data into the Kafka topic.

4. **Configure AWS Glue**: 
   - Set up Glue Crawlers and Glue Catalog for data processing.

5. **Query Data Using Athena**: 
   - Use Athena to query the processed data in S3 for generating insights.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
