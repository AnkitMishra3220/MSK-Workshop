

# Join an Event 

 https://catalog.workshops.aws/


# Create Topic 

    /home/ec2-user/kafka/bin/kafka-topics.sh --create --bootstrap-server $brokers --replication-factor 3 --partitions 1 --topic MSKTutorialTopic

# Produce Messages to MSK Topic 
        
    /home/ec2-user/kafka/bin/kafka-console-producer.sh --broker-list $brokers --topic MSKTutorialTopic

# Consume messages from MSK Topic
        
    /home/ec2-user/kafka/bin/kafka-console-consumer.sh --bootstrap-server $brokers --topic MSKTutorialTopic --from-beginning

# Create another Topic with 5 partitions 

    /home/ec2-user/kafka/bin/kafka-topics.sh --create --bootstrap-server $brokers --replication-factor 3 --partitions 5 --topic test-topic

# Produce messages to MSK Topic with both key and value

    /home/ec2-user/kafka/bin/kafka-console-producer.sh --broker-list $brokers --topic test-topic --property parse.key=true --property key.separator=:

# Consume messages from MSK Topic with both key,value,partition and offset

    /home/ec2-user/kafka/bin/kafka-console-consumer.sh --bootstrap-server $brokers --topic test-topic --formatter kafka.tools.DefaultMessageFormatter --property print.timestamp=true --property print.key=true --property print.value=true --property print.partition=true  --property print.offset=true --from-beginning
