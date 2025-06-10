# 🧠 Java Quiz Microservice System

A scalable microservice-based quiz application built using Spring Boot, Spring Cloud, and Netflix Eureka. It allows creating, managing, and evaluating quizzes based on categorized questions.

## 📚 Table of Contents
- [Tech Stack](#-tech-stack)
- [Microservices](#-microservices)
- [Architecture](#-architecture)
- [Setup Instructions](#-setup-instructions)
- [API Endpoints](#-api-endpoints)
- [Future Enhancements](#-future-enhancements)
- [Author](#-author)
- [License](#-license)

## 🔧 Tech Stack

- Java 17+
- Spring Boot
- Spring Cloud Gateway
- Netflix Eureka
- Maven
- REST APIs

## 🧩 Microservices

### 🧭 API Gateway
- Handles routing to backend services

### 🧾 Service Registry (Eureka)
- Discovers and manages service instances dynamically

### ❓ Question Service
- Manages quiz questions (CRUD + category filtering)

### 📝 Quiz Service
- Creates quizzes and evaluates submissions

## 🏗️ Architecture

```
Client → API Gateway → Quiz Service
                         ↑
                         ↓
                 Question Service
                         ↑
                         ↓
                Eureka Service Registry
```

## 🚀 Setup Instructions

### Prerequisites
- Java 17+
- Maven
- Git

### Steps

1. Clone the repository
```bash
git clone https://github.com/mistrypavankumar/java-quiz-micro-service.git
cd java-quiz-micro-service
```

2. Start Services (in order):
```bash
# Terminal 1
cd service-registry && mvn spring-boot:run

# Terminal 2
cd api-gateway && mvn spring-boot:run

# Terminal 3
cd question-service && mvn spring-boot:run

# Terminal 4
cd quiz-service && mvn spring-boot:run
```

> API Gateway Default Port: `8765`  
> Eureka Dashboard: `http://localhost:8761`

## 🌐 API Endpoints

### Question Service
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/question/all` | Get all questions |
| GET | `/question/category/{category}` | Get questions by category |
| POST | `/question/add` | Add new question |
| GET | `/question/generate` | Generate questions for quiz |
| POST | `/question/getQuestions` | Get questions by ID |
| POST | `/question/getScore` | Submit quiz answers and get score |

### Quiz Service
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/quiz` | Create quiz |
| GET | `/quiz/{id}` | Get quiz by ID |
| POST | `/quiz/{id}/submit` | Submit quiz answers |

## 🔮 Future Enhancements

- Add user authentication and role-based access (JWT)
- Add Docker and Docker Compose support
- React.js-based frontend UI
- Score history per user

## 👨‍💻 Author

**Pavan Kumar Mistry**  
📍 Glassboro, NJ  
📧 mistrypavankumar2304@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/pavan-kumar-mistry-5067b21b1) | [GitHub](https://github.com/mistrypavankumar) | [Portfolio](https://pavankumarmistry-portfolio.vercel.app)

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
