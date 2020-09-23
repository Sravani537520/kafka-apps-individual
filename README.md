# kafka-apps-individual

## kafka commands

### we need to run the commands in different powershell windows

## command to run Zookeeper service

```.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties ```

### To start the kafka service
``` .\bin\windows\kafka-server-start.bat .\config\server.properties ```
### To create a kafka topic
```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic tourist-places```
### To list the created topics 
``` .\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list ```
### To delete the topic 
```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --delete --topic bearcat-messages ```
### To run the producer
This allows you to send the messages to the topic
``` .\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic tourist-places ```
### To run the consumer 
It will display the messages sent to the topic
``` .\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic tourist-places --from-beginning```