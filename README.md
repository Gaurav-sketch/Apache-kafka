# Apache-kafka
<img src="https://miro.medium.com/max/1200/0*9DPCGOCmDvmSEa3H.png" width="100" height="100" />

Working on live data , Gold rates.This project is to track real time Gold price.Creating barplots for all the real time Gold price consumed by consumer.
Need to have two files - Producer and Consumer. 
Send the data and receive the data.

# Packages (Using Python)
- time 
- JSON
- kafka
- datetime
- matplotlib
- pandas
- requests


# Following commands are useful while working from command prompt

# First create the local host :

Start with zookeeper:
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

Start your kafka :
.\bin\windows\kafka-server-start.bat .\config\server.properties

Command to create topic in kafka:
.\bin\windows\kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic TestTopic

list all the topics :
.\bin\windows\kafka-topics.bat --list --zookeeper localhost:2181


# Open the topic and send the message 
.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic TestTopic 


# Now check the consumer 
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic TestTopic --from-beginning








