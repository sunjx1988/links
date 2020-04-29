```yml
version: '3'
services:

  zookeeper:
    image: wurstmeister/zookeeper
    ports:
      - "2181:2181"

  kafka:
    image: wurstmeister/kafka:2.11-0.11.0.3
    ports:
      - "9092"
        environment:
            KAFKA_ADVERTISED_LISTENERS: PLAINTEXT://:9092
            KAFKA_LISTENERS: PLAINTEXT://:9092
            KAFKA_ZOOKEEPER_CONNECT: zookeeper:2181
        volumes:
            - /var/run/docker.sock:/var/run/docker.sock

  jobmanager:
    image: flink:1.7.2-scala_2.12-alpine
    ports:
      - "8081:8081"
    command: jobmanager
    environment:
      - JOB_MANAGER_RPC_ADDRESS=jobmanager

  taskmanager:
    image: flink:1.7.2-scala_2.12-alpine
    command: taskmanager
    environment:
      - JOB_MANAGER_RPC_ADDRESS=jobmanager
```