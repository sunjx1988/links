##  创建一个topic主题
```
docker exec zk-kafka-flink_kafka_1 \
kafka-topics.sh \
--create --topic topic \
--partitions 4 \
--zookeeper zookeeper:2181 \
--replication-factor 1
```

## 创建命令行输入数据的kafka生产者,主题为topic
docker exec -it zk-kafka-flink_kafka_1 \
kafka-console-producer.sh \
--topic topic \
--broker-list zk-kafka-flink_kafka_1:9092

## 创建一个消费者
docker exec zk-kafka-flink_kafka_1 \
kafka-console-consumer.sh \
--topic topic \
--bootstrap-server zk-kafka-flink_kafka_1:9092

```