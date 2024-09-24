# Document Streaming Using FastAPI, Kafka, Spark, MongoDB, Docker

![Document Streaming](https://github.com/user-attachments/assets/adffd5c7-8c5a-41d9-9782-11e52e7dac24)

## Overview
1. **Data Retrieval:** Fetch Data from a text file through an API created using FastAPI.
2. **Data Streaming:** Stream this data to a Kafka topic.
3. **Real Time Processing:** Process this data using Spark structured streaming.
4. **Data Storage:** Store the processed data into MongoDB.

## Creating API using FastAPI
1. The API-Ingest/app/main.py file defines the code for creating the API. It takes data from a python client or postman and sends the data to a kafka topic named ingestion-topic.
2. API-Ingest/dockerfile is used to dockerize the API.

## Running the docker container with the API, Kafka, Spark & MongoDB
1. docker-compose-kafka-spark-mongodb.yml is used to spin up the docker container to execute the pipeline including the API image created in the previous step(the API is configured to run at port number 80).

## Creating ingestion-topic in Kafka and writing data to MongoDB.
1. Run the following command to create the topic ./kafka-topics.sh --create --topic ingestion-topic --bootstrap-server localhost:9092.
2. Run ApacheSpark/02-streaming-kafka-src-dst-mongodb.ipynb jupyter notebook to write data into mongodb.
