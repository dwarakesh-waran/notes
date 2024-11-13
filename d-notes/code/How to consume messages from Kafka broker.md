Topic: [[Kafka]]
1. In order to consume a message from a topic (which is hosted in a Kafka broker), we need to create a consumer and attach it to a Consumer Group Id. 
	1. To create a consumer in java, write a method in a spring boot application and annotate it with @KafkaListener annotation.
2. Then the consumer group ID should subscribe with a specific topic.
	1. As part of the the parameters of @KafkaListener annotation, configure the the consumer group ID and the topic name for which it needs to subscribe. 
3. Then the topic will assign its partitions to the consumers within the consumer group.


