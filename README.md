# End-to-End Data Engineering Pipeline

An end-to-end data engineering project demonstrating how to build a data pipeline using Apache Kafka, Apache Spark, Apache Airflow, PostgreSQL, and Docker.

The project implements a complete workflow for extracting data from an external API, streaming it through Kafka, processing it with Spark, and storing the results in PostgreSQL. Airflow orchestrates the different stages of the pipeline.

## Architecture Overview

The pipeline consists of three main stages:

### 1. Data Ingestion and Streaming
- Extract data from an external API.
- Stream the retrieved data into an Apache Kafka topic.
- Use Kafka as the messaging layer between data ingestion and processing.

### 2. Data Processing and Storage
- Apache Spark consumes messages from the Kafka topic.
- Process and transform the incoming data.
- Load the processed records into a PostgreSQL database.
- Make the resulting data available for downstream applications.

### 3. Workflow Orchestration
- Use Apache Airflow to orchestrate the pipeline.
- Schedule the API extraction and Kafka streaming tasks.
- Trigger Spark processing after data ingestion is completed.
- For demonstration purposes, the streaming process is scheduled daily rather than running continuously.

## Technology Stack

| Technology | Purpose |
|---|---|
| Apache Kafka | Real-time data streaming and message management |
| Apache Spark | Distributed data processing and transformation |
| Apache Airflow | Workflow orchestration and scheduling |
| PostgreSQL | Relational database for processed data |
| Docker | Containerization of individual services |
| Docker Compose | Management of the multi-container environment |

## Pipeline Architecture


## Execution Workflow

The pipeline follows this execution sequence:

1. Airflow triggers the data extraction task.
2. The API data is retrieved and published to a Kafka topic.
3. Once ingestion is completed, Airflow triggers the Spark processing job.
4. Spark consumes the Kafka messages and performs the required transformations.
5. Processed data is written into PostgreSQL.
6. The resulting dataset becomes available for downstream applications, including LLM-based applications.

## Deployment

All infrastructure components are containerized and deployed using Docker Compose.

This approach provides:
- Consistent execution environments.
- Simplified service management.
- Reproducible infrastructure.
- Easier deployment and development.

## Getting Started

For a detailed, step-by-step implementation guide, refer to the original tutorial:


## Project Goals

This project demonstrates the integration of several essential data engineering technologies into a unified pipeline, covering:

- API-based data ingestion.
- Event streaming with Kafka.
- Distributed data processing with Spark.
- Workflow orchestration with Airflow.
- Relational data storage with PostgreSQL.
- Containerized infrastructure with Docker.

---