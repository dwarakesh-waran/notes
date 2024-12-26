Topic: [[My Project]]

### Problem Statement
We have a theatre owner. The owner produces cinema tickets. Then he wants to send the tickets to the film buffs. He needs to have an application which regulates this transfer in a smooth way.

### Introducing Kafka
1. A Kafka producer Spring Boot Application will produce tickets.
2. The ticket should have the following values.
	- ticketId
	- movieName
	- auditoriumNumber
	- ticketPrice
	- showTime
3. Producers can create individual ticket for each movie and it can create multiple tickets for each movie and store it in the Kafka Server.
4. This information will be serialized into avro format and will be sent as a message to a Kafka server (preferably running in a docker container).
5. Each [[Topic]] in the Kafka Server represents the the Auditorium Number. There are three types of Auditoriums available in the movie theatre.
	- IMAX
	- Standard
	- 3D
6. Each [[Partition]] inside the topic represents the Show Time. There are 3 Showtimes available in an auditorium.
	- Morning Show (10 AM)
	- Matinee Show (2 PM)
	- Evening Show (6 PM)
7. A Kafka Consumer Spring Application will purchase these tickets.
8. We are groups of people who purchase tickets based on the type of the screen. So, there are 3 types of consumer groups.
	- ImaxGroup
	- StandardGroup
	- 3dGroup




This project is developed to learn about [[Kafka]]

1. Write a Dockerfile for kakfa server and run it
2. Create a Kafka producer using Spring Boot
3. Write a Dockerfile and deploy the producer in the Docker Container
4. Create a Kafka consumer using Spring Boot
5. Write a Dockerfile and deploy the consumer in the Docker Container