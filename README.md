# Kafka
 step-by-step guide to running Kafka, Zookeeper, creating topics, and producing/consuming messages
Sure, here's a step-by-step guide to running Kafka, Zookeeper, creating topics, and producing/consuming messages:
Start Zookeeper:
Navigate to your Kafka installation directory.
Run Zookeeper using the following command:
bin/zookeeper-server-start.sh config/zookeeper.properties
          Start Kafka Broker:
Open a new terminal window or tab.
Navigate to your Kafka installation directory.
Run Kafka broker using the following command:
bin/kafka-server-start.sh config/server.propertiesconfig/server.properties
Create a Kafka Topic:
Open a new terminal window or tab.
Navigate to your Kafka installation directory.
Use the kafka-topics.sh script to create a topic. Replace your_topic_name with the name you want to give to your topic.
bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic your_topic_name
Start a Kafka Producer:
Open a new terminal window or tab.
Navigate to your Kafka installation directory.
Run the Kafka console producer to start producing messages to the topic. Replace your_topic_name with the name of the topic you created in the previous step.bin/kafka-console-producer.sh --bootstrap-server localhost:9092 --topic your_topic_name
Start a Kafka Consumer:
Open a new terminal window or tab.
Navigate to your Kafka installation directory.
Run the Kafka console consumer to start consuming messages from the topic. Replace your_topic_name with the name of the topic you created.
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic your_topic_name --from-beginning
Now you have Zookeeper, Kafka broker, a topic created, a producer publishing messages to the topic, and a consumer consuming messages from the topic. You can start typing messages in the producer terminal, and you should see them being consumed by the consumer in real-time.

