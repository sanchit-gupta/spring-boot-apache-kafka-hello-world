Kafka:

./gradlew jar -PscalaVersion=2.12.10
./bin/zookeeper-server-start.sh ./config/zookeeper.properties
/opt/kafka-2.4.0-src$./bin/kafka-server-start.sh ./config/server.properties
./bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic javainuse-topic
./bin/kafka-console-producer.sh --broker-list localhost:9092 --topic javainuse-topic
./bin/kafka-console-consumer.sh  --bootstrap-server localhost:9092 --topic javainuse-topic --from-beginning



For application output:
./bin/kafka-console-consumer.sh  --bootstrap-server localhost:9092 --topic java_in_use_topic --from-beginning