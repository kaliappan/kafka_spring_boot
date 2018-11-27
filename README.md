# kafka_spring_boot
Simple Spring Boot demo project with Apache Kafka

How to Work with Apache Kafka in Your Spring Boot Application.

Prerequisites:
Confluent Kafka:
1. Download
2. Unzip it
3. Kafka up and running in your local environment 
Confluence_Kafka/confluent-4.1.1# confluent start
ksql-server is [UP]
connect is [UP]
kafka-rest is [UP]
schema-registry is [UP]
kafka is [UP]
zookeeper is [UP]

Kafka topic name: users

Spring Boot application with a Kafka producer to publish messages to your Kafka topic, as well as with a Kafka consumer to read those messages.

Step 1: Generate project

Step 2: Publish/read messages from the Kafka topic

Step 3: Configure Kafka through application.yml configuration file

Step 4: Create a producer

  1.Creating a producer will write our messages to the topic(users)
  2.Auto-wired KafkaTemplate and will use this instance to publish messages to the topic—that’s it for producer!

Step 5: Create a consumer

  Consumer is  the service that will be responsible for reading messages processing them according to the needs of your own business logic.
  void consume (String message) to subscribe to the user’s topic and just emit every message to the application log. In your real application, you can handle messages the way your business requires you to.

Step 6: Create a REST controller

Step 7: Let’s send our message to Kafka using cURL:
  curl -X POST -F 'message=test' http://localhost:9000/kafka/publish
  
 INFO 5078 --- [nio-9000-exec-2] com.example.engine.Producer              : #### -> Producing message -> test
 INFO 5078 --- [nio-9000-exec-2] o.a.k.clients.producer.ProducerConfig    : ProducerConfig values: 
 INFO 5078 --- [ntainer#0-0-C-1] com.example.engine.Producer              : #### -> Consumed message -> test
