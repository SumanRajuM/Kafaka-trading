# Kafaka-trading
practice kafaka 


sh zookeeper-server-start.sh /Users/suman/softDev/SumanDev/kafaka/kafka_2.13-3.8.0/config/zookeeper.properties
sh kafka-server-start.sh   /Users/suman/softDev/SumanDev/kafaka/kafka_2.13-3.8.0/config/server.properties

# create the topic 
suman@Muppallas-MacBook-Pro bin % sh kafka-topics.sh --bootstrap-server localhost:9092 --topic order_trading  --create --partitions 3 --replication-factor 1
suman@Muppallas-MacBook-Pro bin % sh kafka-topics.sh --bootstrap-server localhost:9092 --topic position_trading  --create --partitions 3 --replication-factor 1
kafka-topics.sh --bootstrap-server localhost:9092 --topic first_topic --create --partitions 3 --replication-factor 1

list of Topics:
---------------
sh kafka-topics.sh --bootstrap-server localhost:9092 --list

sh kafka-topics.sh --bootstrap-server localhost:9092  --describe topic order_trading 

kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic first_topic

kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic first_topic --from-beginning

kafka-console-producer.sh --bootstrap-server localhost:9092 --topic first_topic

