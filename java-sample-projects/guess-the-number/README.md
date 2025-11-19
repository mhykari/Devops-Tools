# 🎮 Guess The Number – Spring Boot Mini Game

A minimal, lightweight **Spring Boot 3** application where the user tries to guess a secret number (1–100).  
This project is perfect for:

- Learning Spring Boot  
- Testing REST APIs  
- Practicing Java basics  
- Docker deployment demos  
- Lightweight backend examples  

The application includes both:
- 🧠 REST API  
- 🌐 Simple HTML UI served from `/`  

---

## 🚀 Features

- Random secret number generated at startup  
- Guess via REST API  
- Reset the game anytime  
- Tracks number of attempts  
- Simple static HTML interface  
- Lightweight Docker image  
- Very small codebase and easy to understand  

---

## 📦 Project Structure

src/
├── main
│ ├── java/com/example/game
│ │ ├── GameApplication.java
│ │ ├── controller/GameController.java
│ │ └── service/GameService.java
│ └── resources/static/index.html
├── test/java/com/example/game/GameServiceTest.java
pom.xml
Dockerfile
README.md

---

## 🛠 Requirements

- Java **17+**
- Maven **3.8+**
- (Optional) Docker for containerization

---

# 🧩 Running the Application

## 1️⃣ Build the application

mvn clean package

This command generates:
target/guess-number-1.0.jar

## 2️⃣ Run the application

Default port (8080):
java -jar target/guess-number-1.0.jar
or
Custom port example:
java -jar target/guess-number-1.0.jar --server.port=8085

---

# 🌐 Using the Application
Once running, open the browser:
http://localhost:8080/

## 📌 REST API Endpoints
🎯 Guess a number
GET /game/guess?number=50

🔄 Reset the game
POST /game/reset

🔢 Get attempts count
GET /game/attempts

---

## 🐳 Docker Support
A lightweight Dockerfile is included in the files.

## Build Docker image:
docker build -t guess-number .
Run container:
docker run -p 8080:8080 guess-number

Custom port:
docker run -p 8085:8080 guess-number

## 🧪 Running Tests
mvn test  
Unit tests are included in:  
src/test/java/com/example/game/GameServiceTest.java  