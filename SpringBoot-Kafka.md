Spring has a special class called KafkaTemplate that publishes data to Kafka.
KafkaTemplate is an abstraction over kafka client, which contains several classes that handle publish to Kafka.
send() method in KafkaTemplate converts the parameters into ProducerRecord class and sends the messages to the respective kafka topic.

We dont need to maintain connection with Kafka. Spring automatically does it.
@Autowired : Spring will create and inject HelloKafkaProducer to be used.
@KafkaListener: It is specified before the method, so that the method will consume messages from a topic.

Spring consumer requires to define group id, which means we have to define consumer group for each of our consumer.
We can define group ID for the whole consumer application or define for each kafka listener.

Spring has annotation for scheduling known as @Scheduled

@EnableScheduling annotation is used to enable the scheduler for your application. 
This annotation should be added into the main Spring Boot application class file. 

Question:
Producer has produced messages on to Kafka and let's say consumer is not running. Producer is stopped and when the consumer is begin to run, surprisingly
it doesnt seem to consume messages although data available on Kafka.

When consumer is running and producer starts to produce the messages, we can see consumer consuming the messages.

How to fix this ?
When the consumer is started for  the first time there is not committed offset position. Hence we need to tell the consumer where to start consuming messages 
by setting "auto.offset.reset" configuration. There are 2 values commonly used for this configuration -
earliest, latest.
Default is latest => if there is no committed position, consumer will start receiving and processing messages that are sent to kafka after consumer 
started.


If we need consumer to consume all the messages produced even before consumer started, set the auto.offset.reset to "earliest"



