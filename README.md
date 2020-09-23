# kafka-apps-individual

## kafka commands

### we need to run the commands in different powershell windows

### Command to run Zookeeper service

```.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties ```

### Command to start the kafka service
``` .\bin\windows\kafka-server-start.bat .\config\server.properties ```
### Command to create a kafka topic
```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic tourist-places```
### Command to list the created topics 
``` .\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list ```
### Command to delete the topic 
```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --delete --topic bearcat-messages ```
### Command to run the producer
This allows you to send the messages to the topic

``` .\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic tourist-places ```
### Command to run the consumer 
It will display the messages sent to the topic

``` .\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic tourist-places --from-beginning```
