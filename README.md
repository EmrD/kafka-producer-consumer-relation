# Kafka Producer - Consumer Relation

This is an simple repository that uses Kafka. This repository uses Kafka topics to communicate. 

## What is Kafka?

Apache Kafka is a distributed event streaming platform capable of handling trillions of events a day. It is designed for high-throughput, fault-tolerant, and scalable messaging between applications. Kafka is widely used for building real-time data pipelines and streaming applications. It provides a unified platform for handling real-time data feeds and supports various use cases like logging, data integration, and monitoring.

## Running On Local Environment

To test locally. Run;

Download Kafka;

- `wget https://downloads.apache.org/kafka/3.8.1/kafka_2.12-3.8.1.tgz`

Extract Kafka files;

- `tar -xf kafka_2.12-3.8.1.tgz` 

Enter the directory;
- `cd kafka_2.12-3.8.1`

Start Kafka services;
- `bin/zookeeper-server-start.sh ./config/zookeeper.properties`

Start Kafka server;
- `bin/kafka-server-start.sh config/server.properties`

Create topic;
- `bin/kafka-console-producer.sh --topic my-topic --bootstrap-server localhost:9092`

Listen your topic;
- `bin/kafka-console-consumer.sh --topic my-topic --bootstrap-server localhost:9092 --from-beginning`

You must see your test messages on listener console. 
