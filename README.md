## Overview

This project implements a simple database client-server application using C. The server handles multiple clients concurrently, processing PUT and GET requests to store and retrieve data.

## Files

- dbserver.c: Server implementation.
   
- dbclient.c: Client implementation.
   
- Makefile: Build instructions.
   
- msg.h: Header file containing message definitions and structures.
   
- common_threads.h: Header file containing threading utilities.
  
## Features
- Multithreading on the server to handle multiple clients concurrently.
- Client-server communication using sockets.
- Database operations: PUT to store data and GET to retrieve data.

## Build Instructions

To compile the server and client, use the provided Makefile:
~~~
make
~~~
This will generate the dbserver and dbclient executables.

## Usage


Start the server:
~~~
./dbserver <port>
~~~
Replace <port> with the desired port number.

Start the client:
~~~
./dbclient <server_ip> <port>
~~~

Replace <server_ip> with the server's IP address and <port> with the server's port number.
  
### The client supports the following commands:
~~~
PUT <key> <value>
~~~
Store the value with the specified key.
~~~
GET <key>
~~~
Retrieve the value associated with the specified key.
