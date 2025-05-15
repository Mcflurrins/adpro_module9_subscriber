##  What is amqp? 
AMQP (Advanced Message Queuing Protocol) is an open standard application layer protocol for message-oriented middleware. It enables applications to communicate through message brokers by handling messages between different systems.

## What does it mean? guest:guest@localhost:5672 , what is the first guest, and what is the second guest, and what is localhost:5672 is for? 
This is an AMQP URI for conencting to a RabbitMQ server.
The first "guest" in "guest:guest@localhost:5672" is the username for authentication to the message broker. In many message broker systems (like RabbitMQ), "guest" is the default username. 
The second "guest" after the colon is the password for authentication. This also usually comes as the default password to the "guest" username. 
In "localhost:5672", "localhost" is the hostname (meaning the message broker is running on my local machine) and "5672" is the port number. Port 5672 is the default port used by AMQP for non-TLS connections. To connect to a remote server instead, I can replace "localhost" with the server's IP address or domain name.

![image](https://github.com/user-attachments/assets/b0d7641f-dd51-4458-8879-845d724f8f77)
I got 30 queues because I ran `cargo run` at least 6 times in the publisher folder. Since the subscriber is slow now, it can't process messages as fast as they are sent from the publisher, so unprocessed requests go into the queue first. 
