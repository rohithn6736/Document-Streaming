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
