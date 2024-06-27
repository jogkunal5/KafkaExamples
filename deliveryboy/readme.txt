Kafka:


- Zookeper start command

C:\WorkSpace\kafka_2.12-3.4.0>bin\windows\zookeeper-server-start.bat config\zookeeper.properties

- Kafka server start command:

C:\WorkSpace\kafka_2.12-3.4.0>bin\windows\kafka-server-start.bat config\server.properties

- Topic create command

Go to C:\WorkSpace\kafka_2.12-3.4.0\bin\windows> kafka-topics.bat --create --topic user-topic --bootstrap-server localhost:9092

Here user-topic is the name of topic.

On command prompt it will display like this once topic created:

Created topic user-topic.

- Produce new topic

C:\WorkSpace\kafka_2.12-3.4.0\bin\windows>kafka-console-producer.bat --topic user-topic --bootstrap-server localhost:9092
>Hi
>hello
>how
>are
>you
>dear
>kafka

- Consume above topic messages (open new terminal window)

C:\WorkSpace\kafka_2.12-3.4.0\bin\windows>kafka-console-consumer.bat --topic user-topic --from-beginning --bootstrap-server localhost:9092
Hi
hello
how
are
you
dear
kafka


- To consume only the latest message from a Kafka topic, you can use the --max-messages option with a value of 1. This will consume only the latest message from the topic.Here's an example command:

kafka-console-consumer.bat --topic location-update-topic --bootstrap-server localhost:9092 --max-messages 1
