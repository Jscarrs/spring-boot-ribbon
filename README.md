# Spring Boot Ribbon Load Balancer with Eureka

This project demonstrates client-side load balancing using **Spring Cloud Ribbon** and **Eureka Service Discovery**.

## Architecture

The system contains three main components:

- **Eureka Server** – Service registry where services register.
- **Ribbon Servers (2 instances)** – Backend services running on different ports.
- **Ribbon Client** – Calls the servers through Ribbon load balancing.

## Servers

Two instances of the server are running:

- Server 1 → http://localhost:9090  
- Server 2 → http://localhost:9091  

Both servers register themselves with **Eureka**.

## Client

The client application runs on:

- http://localhost:8888

The client uses **Ribbon** to distribute requests between the two servers.

It shows the registered services:

- CLIENT
- SERVER (9090)
- SERVER (9091)

## Technologies Used

- Java (Prior to Java 17 as required)
- Spring Boot
- Spring Cloud Netflix Eureka
- Spring Cloud Ribbon
- Maven

## How to Run

1. Start **Eureka Server**
2. Start **Ribbon Server** on port `9090`
3. Start another **Ribbon Server** on port `9091`
4. Start the **Ribbon Client**
5. Open Eureka dashboard:
http://localhost:8761

## Author

Scarlett Jet
