# MSK-Workshop

Join an Event - https://catalog.workshops.aws/



cd /home/ec2-user/kafka

Create Topic 

bin/kafka-topics.sh --create --bootstrap-server $brokers --replication-factor 3 --partitions 1 --topic MSKTutorialTopic

Produce Messages to MSK Topic 
bin/kafka-console-producer.sh --broker-list $brokers --topic MSKTutorialTopic

Consume messages from MSK Topic
bin/kafka-console-consumer.sh --bootstrap-server $brokers --topic MSKTutorialTopic --from-beginning
