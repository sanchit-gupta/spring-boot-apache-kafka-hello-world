List of Important Command to setup Kafka on Linux System:



1. ./gradlew jar -PscalaVersion=2.12.10
2. ./bin/zookeeper-server-start.sh ./config/zookeeper.properties
3. ./bin/kafka-server-start.sh ./config/server.properties
4. ./bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic javainuse-topic
5. ./bin/kafka-console-producer.sh --broker-list localhost:9092 --topic javainuse-topic
6. ./bin/kafka-console-consumer.sh  --bootstrap-server localhost:9092 --topic javainuse-topic --from-beginning



For application output:
1. ./bin/kafka-console-consumer.sh  --bootstrap-server localhost:9092 --topic java_in_use_topic --from-beginning


This demo is inspired from below links;

https://www.javainuse.com/misc/apache-kafka-hello-world
https://www.javainuse.com/spring/spring-boot-apache-kafka-hello-world