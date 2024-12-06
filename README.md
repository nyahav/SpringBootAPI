# 🎉 **Basic Spring Boot Application with Docker, Postgres, AWS, and Microservices**

Welcome to the **Basic Spring Boot Application** project! This repository demonstrates a comprehensive backend application built with **Spring Boot**, **PostgreSQL**, **Docker**, **Microservices**, **JWT**, and **CI/CD** integration. It’s designed to showcase your skills in backend development, containerization, and cloud deployment.

### 🚀 **Project Overview**
This project implements a **RESTful CRUD API** for managing `Students` with features like **Swagger UI**, **Spring Data JPA**, **Pagination & Sorting** (FPS), **SMS integration** via **Async**, **JWT Authentication**, and **Microservices Architecture**. It’s Dockerized for easy deployment and also includes integration with **AWS S3** and **Jenkins** for CI/CD.

---

## 🛠️ **Technologies Used**

### **Backend Technologies:**
- **Java** 🟨 (JDK 11)
- **Spring Boot 2.5.2** ⚡️
- **Spring Data JPA** 📊
- **Spring Security & JWT** 🔐
- **Spring Actuator** 📈
- **Spring Swagger** 📝

### **Database:**
- **PostgreSQL** 🗄️
- **Spring Data PostgreSQL** 🌱

### **Containerization & Deployment:**
- **Docker** 🐋
- **Docker Compose** ⚙️
- **AWS EC2** ☁️
- **AWS S3** 🛒

### **Microservices & Messaging:**
- **Microservices Architecture** 💥
- **JWT Authentication** 🔑
- **SMS Integration** (Async) 📱

### **Testing & CI/CD:**
- **Postman** 📬
- **Newman** 📊
- **Jenkins** 🏗️

---

## 🚀 **Getting Started**

To get started with the project, follow the steps below to set up the environment and run the application locally or in the cloud.


2️⃣ Install Dependencies:

You can either run the app using Docker or directly with Spring Boot.
Using Docker:

    Start Docker Container for PostgreSQL:

docker run -d -p 5432:5432 -v postgresdata:/var/lib/postgresql/data -e POSTGRES_PASSWORD=postgres postgres

    Start the Application with Docker Compose:

docker-compose up -d

Running Directly with Spring Boot:

If you're running without Docker, make sure you have Java 11 installed and run:

./mvnw spring-boot:run

3️⃣ Access Swagger UI:

Once the app is running, navigate to the following URL to explore the API and its documentation:

http://localhost:8080/swagger-ui.html

🛠️ Application Features
🌐 RESTful API with Swagger

    The application provides a RESTful API for performing CRUD operations on Students.
    Swagger UI is enabled for easy API documentation and testing.

🗂️ Database Management with PostgreSQL

    The app uses Spring Data JPA to interact with a PostgreSQL database.
    Database connection is configured through application.properties.

📑 Filter, Pagination, and Sorting (FPS)

    Implemented simple filters, pagination, and sorting on the Student entity to make data retrieval more efficient.

🔐 JWT Authentication

    Secure the application using JWT Authentication.
    Access tokens are issued to authenticate users and restrict unauthorized access.

🔄 Microservices Architecture

    The project is designed to be extensible with Microservices using separate services for different functionalities (e.g., SMS integration, students CRUD).

📱 SMS Integration (Async)

    The app includes SMS functionality using the SMS4Free API for sending messages asynchronously. The integration is configured in SmsService.java.

🚚 Dockerized Application

    Both the Spring Boot application and PostgreSQL are containerized with Docker and Docker Compose.
    This ensures easy deployment and management of the services.

📝 Commit History

    Commit 1: 🎉 Hello World with Spring Boot
    Commit 2: 📄 Add Swagger for API Documentation
    Commit 3: 🐳 Docker Setup for Postgres
    Commit 4: 🔄 Integrate Spring Data JPA with PostgreSQL
    Commit 5: 🔐 Implement JWT Authentication
    Commit 6: 💥 Microservices Architecture & SMS Integration
    Commit 7: 🚀 Docker Compose for Easy Deployment
    Commit 8: 📊 Add Test Coverage & Postman Integration
    Commit 9: ☁️ Deploy to AWS EC2 using Docker

🏗️ Continuous Integration and Deployment

🧑‍💻 Jenkins Setup

    Jenkins is integrated for Continuous Integration (CI) and Continuous Deployment (CD) to automatically build, test, and deploy the application.
    Pull requests are automatically built and tested through Jenkins.

🚀 Docker and AWS EC2 Deployment

    The Dockerized application is deployed on AWS EC2.
    After building the Docker image, it is pushed to Docker Hub and pulled to an EC2 instance for cloud deployment.

🔑 Environment Variables

In application.properties, configure the following for your local or production environment:

# Database Configuration
spring.datasource.url=jdbc:postgresql://localhost:5432/postgres
spring.datasource.username=postgres
spring.datasource.password=postgres
spring.datasource.driver-class-name=org.postgresql.Driver

# JWT Configuration
jwt.secret=your-secret-key

# SMS Integration (Async)
can't add this here-make your own

🔧 Useful Commands

    Docker Compose (Start Services)

docker-compose up -d

    Docker Build (Build Image)

docker build . -t basic-spring

    Jenkins Build

    Trigger a Jenkins build using the configured pipeline for testing and deployment.

    Postman/Newman (Run Tests)

docker exec niv-basicspring_newman_1 newman run STUDENTS_TEST.postman_collection.json --reporters cli,junit,htmlextra --reporter-junit-export "newman/report.xml" --reporter-htmlextra-export "newman/report.html"

🌟 Contributing

We welcome contributions to improve the project. To contribute:

    Fork this repository.
    Create a new branch for your feature or bug fix.
    Open a pull request for review.

📄 License

This project is licensed under the MIT License.

Thank you for checking out this project! 🚀

### 1️⃣ **Clone the Repository:**
```bash
git clone https://github.com/your-username/basic-spring.git
cd basic-spring
