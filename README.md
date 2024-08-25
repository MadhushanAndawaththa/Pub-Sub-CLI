# Pub-Sub-CLI
simple Publish and Subscribe  middleware using Client-Server Sockets Programming concepts and techniques


# Task 1: The Client-Server Application
1. Implement a client-server socket application using the selected programming language. 
The server will listen for connections on a pre-defined PORT where the client will use the 
server IP and the PORT to connect to the server.

# Task 2: Publishers and Subscribers
1. Improve the client-server implementation for the Server to handle multiple concurrent 
Client connections.
2. Multiple client applications should be able to connect to the server and the typed text in a 
given client CLI should be displayed on the Server terminal CLI.
3. The client application should take the third command line argument to indicate whether 
the client will act as either “Publisher” or “Subscriber”.
E.g. 
my_client_app 192.168.10.2 5000 PUBLISHER
my_client_app 192.168.10.2 5000 SUBSCRIBER
4. Further, the server should echo the messages sent by any “Publisher” clients to all the 
“Subscriber” clients’ terminals. For example, when a single server is connected with 10 
client applications when a client terminal that is in Publisher mode types a text, it should 
be displayed on all remaining client terminals that are connected as Subscribers.
5. The Publisher messages should be only shown on Subscriber terminals, not on any 
Publisher terminals.

# Task 3: Publishers and Subscribers Filtered on Topics/Subjects
1. Improve the implementation of Task 2 to include “topic/subject” based filtering of 
messages among Publishers and Subscribers.
2. The client implementation should be improved to include the fourth command line 
argument of the topic/subject of either the publisher or subscriber.
E.g. 
my_client_app 192.168.10.2 5000 PUBLISHER TOPIC_A
my_client_app 192.168.10.2 5000 SUBSCRIBER TOPIC_A
3. The client application that is a publisher should be sending the messages to the server on 
a specific topic/subject to route to interested subscriber clients on the same topic/
subject.
4. There can be publishers and subscribers interested in different messages connected 
concurrently to the server.
