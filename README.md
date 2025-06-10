## Java Quiz Microservice Project

A Spring Boot-based microservice application for conducting quizzes.

### 🧩 Microservices

- **API Gateway**
  - Routes client requests to microservices
  - Uses Spring Cloud Gateway

- **Service Registry**
  - Eureka-based service discovery for registering microservices

- **Question Service**
  - REST APIs for managing questions
  - Stores questions with difficulty levels and topics

- **Quiz Service**
  - Creates quizzes with questions fetched from Question Service
  - Evaluates user submissions

### 🔧 Tech Stack
- Java 17+
- Spring Boot
- Spring Cloud (Gateway, Eureka)
- REST APIs
- Maven
- Eureka Server
