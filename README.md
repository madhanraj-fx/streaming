# streaming

  
##### KAFKA ########

To Start Zoo Keeper
-------------------
sh bin/zookeeper-server-start.sh config/zookeeper.properties


To Start Kafka Server
---------------------
sh bin/kafka-server-start.sh config/server.properties


To Create a topic in Kafka
--------------------------
bin/kafka-topics.sh --create --zookeeper <ZOOKEEPER_URL:PORT> --replication-factor <NO_OF_REPLICATIONS> --partitions <NO_OF_PARTITIONS> --topic <TOPIC_NAME>

bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic sampleTopic


Describe a Topic :
------------------
bin/kafka-topics.sh --describe --zookeeper localhost:2181 --topic sampleTopic


Create Consumer Group:
----------------------
bin/kafka-console-consumer.sh --bootstrap-server localhost:2181 --topic sampleTopic --consumer-property group.id=sampleGroup


Describe Consumer Group:	
------------------------
bin/kafka-consumer-groups.sh --bootstrap-server local-host:2181 --describe --group sampleGroup


Create a Kafka Console Producer:
--------------------------------
bin/kafka-console-producer.sh --broker-list localhost:9091 --topic sampleTopic


Create a Kafka Console Consumer:
--------------------------------
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic sampleTopic --from-beginning


