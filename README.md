# docker-kafka
Example of docker kafka setup

# Terminal Commands
* docker-compose up -d - run zookeeper and kafka in detached mode
* nc -z localhost 22181 - verify zookeeper service
* nc -z localhost 29092 - verify kafka service
* nc -z localhost 28080 - verify kafka ui
* docker-compose logs kafka | grep -i started - verify kafka started

# Kafka UI
http://localhost:28080

# Configuration
- zookeeper instances: 3
- kafka brokers: 3
- kafka-ui: 1
- security protocol: PLAINTEXT
- offsets.topic.replication.factor: 2, the number of alive brokers has to be at least the replication factor at the time of the first request for the offsets topic
- num.partitions: 3, the default number of log partitions per topic
- min.insync.replicas: 1, the minimum number of in-sync replicas required to exist for a broker to allow acks=all
- offsets.commit.required.acks: -1, the number of acknowledgements that are required before the offset commit can be accepted
