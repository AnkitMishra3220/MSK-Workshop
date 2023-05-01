

# Join an Event 

 https://catalog.workshops.aws/


# Create Topic 

    /home/ec2-user/kafka/bin/kafka-topics.sh --create --bootstrap-server $brokers --replication-factor 3 --partitions 1 --topic MSKTutorialTopic

# Produce Messages to MSK Topic 
        
    /home/ec2-user/kafka/bin/kafka-console-producer.sh --broker-list $brokers --topic MSKTutorialTopic

# Consume messages from MSK Topic
        
    /home/ec2-user/kafka/bin/kafka-console-consumer.sh --bootstrap-server $brokers --topic MSKTutorialTopic --from-beginning
