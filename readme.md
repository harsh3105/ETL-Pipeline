# Real-Time Sales Streaming

## Introduction
Welcome to "Real-Time Sales Streaming", a comprehensive guide designed to help beginners in data engineering build a robust streaming pipeline. This project utilizes a range of Apache Open Source tools, including FastAPI, Kafka, Spark, Cassandra, MySQL, Superset, and Docker, to create a fully functional streaming data pipeline.

## Project Overview
"Real-Time Sales Streaming" is a step-by-step project that demonstrates how to build and deploy a single-node streaming pipeline. Key components of this project include setting up Kafka and Zookeeper, integrating FastAPI with Kafka for real-time data ingestion, establishing data persistence layers using Cassandra and MySQL, and performing data processing and analysis with Spark Streaming. Additionally, the project covers the setup of a visualization layer using Superset, all within a Dockerized environment for streamlined deployment.

## Architecture
The pipeline starts with data ingestion through FastAPI, feeding into Kafka. Spark then processes this streaming data, storing the raw data in Cassandra and aggregating data in MySQL. Finally, Superset is used for visualizing and analyzing the data.

## Directory Structure
Below is the directory structure of the "Real-Time Sales Streaming" project, providing a quick overview of the key components and their organization:
.
├── cassandra
│ └── cassandra-init.sh # Initialization script for Cassandra
├── fastapi-producer
│ ├── scripts
│ │ └── main.py # Main script for FastAPI producer
│ ├── Dockerfile # Dockerfile for FastAPI setup
│ └── requirements.txt # Dependencies for FastAPI producer
├── kafka
│ └── kafka-setup.sh # Setup script for Kafka
├── mysql
│ └── init.sql # Initialization SQL script for MySQL
├── spark-streaming
│ ├── scripts
│ │ ├── consumer.py # Spark consumer script
│ │ └── customers.csv # Sample data
│ └── spark-setup.sh # Setup script for Spark
├── superset
│ ├── dashboard
│ │ ├── scripts
│ │ │ ├── create_dashboard.py # Script to create Superset dashboard
│ │ │ └── supersetapi.py # Superset API client script
│ │ └── Dockerfile # Dockerfile for Superset dashboard
│ ├── Dockerfile # Dockerfile for Superset setup
│ ├── superset_config.py # Superset configuration
│ └── superset-init.sh # Initialization script for Superset
└── docker-compose.yml # Docker Compose configuration file



## Prerequisites
- Docker installed on your system
- Basic familiarity with Docker Compose
- Understanding of Kafka, Pyspark, Cassandra, MySQL, and Superset

## Setup Instructions
1. **Kafka and Zookeeper**: Utilize Bitnami docker images for setup.
   - Follow the provided YAML configurations.
2. **FastAPI and Kafka Integration**: Implement a producer in FastAPI to send messages to Kafka.
   - Refer to the provided Pydantic model and Dockerfile.
3. **Data Persistence Layer**: Use Cassandra for raw data storage and MySQL for aggregated data.
   - Adhere to the docker compose configurations.
4. **Spark Streaming Integration**: Connect Spark with Kafka, Cassandra, and MySQL.
   - Setup the Spark Docker environment and consumer service.
5. **Visualization with Superset**: Visualize data using Superset.
   - Follow the docker compose configurations and setup scripts.

## Running the Project
Execute the following commands to start the project:

```bash
docker compose build
docker compose up -d
```

After starting the containers, interact with the FastAPI endpoint and access the Superset dashboard for real-time data visualization.

## Conclusion
By completing the "Real-Time Sales Streaming" project, you've taken a significant step in the world of data engineering. Continue to explore and develop more complex and innovative data engineering solutions.

## References
- [YouTube Playlist on Data Streaming](https://www.youtube.com/playlist?list=PLe1T0uBrDrfOYE8OwQvooPjmnP1zY3wFe)
- [Apache Spark Structured Streaming Via Docker Compose](https://github.com/zekeriyyaa/Apache-Spark-Structured-Streaming-Via-Docker-Compose)
