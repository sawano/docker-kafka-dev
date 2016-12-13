Image to use for testing and exploring Kafka with minimum hassle.
Contains all you need to run Kafka, kafka-monitor, and kafka manager.

Includes Kafka (with Zookeeper), kafka-monitor, and kafka manager.

## Why a docker image?
To get rid of the hassle/time of installing and building the tools included.
Care have been taken to make the image size as small as possible.

`/kafka/start_all.sh` will start up a Kafka cluster with 3 brokers

## Links
Refer to documentation to start playing around if you're new to Kafka:
* [https://kafka.apache.org/quickstart](https://kafka.apache.org/quickstart)
* [https://github.com/linkedin/kafka-monitor](https://github.com/linkedin/kafka-monitor)
* [https://github.com/yahoo/kafka-manager](https://github.com/yahoo/kafka-manager)

## Quickstart commands:

    docker run -it -p 2181:2181 -p 9092:9092 -p 9093:9093 -p 9094:9094 -p 8000:8000 -p 9000:9000 --name kafka-dev sawano/kafka-dev:0.10.1.0
    /kafka/start_all.sh
    /kafka-monitor/start.sh
    http://localhost:8000/index.html  (kafka-monitor)
    /kafka-manager/start.sh
    http://localhost:9000/  (kakfa-manager)
