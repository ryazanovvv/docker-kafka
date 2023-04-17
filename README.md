# docker-kafka
Example of docker kafka setup

# Terminal Commands
* docker-compose up -d - run zookeeper and kafka in detached mode
* nc -z localhost 22181 - verify zookeeper service
* nc -z localhost 29092 - verify kafka service
* nc -z localhost 28080 - verify kafka ui
* docker-compose logs kafka | grep -i started - verify kafka started

# Kafka UI
Available: http://localhost:28080
