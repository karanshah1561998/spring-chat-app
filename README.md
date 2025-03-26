# 💬 Spring Boot Chat App

A real-time chat application built with **Spring Boot**, **WebSockets**, and **STOMP messaging protocol**. This project demonstrates how to build a scalable backend for a chat system with real-time communication capabilities.

---

## 🚀 Live Demo

**🔗 [https://spring-chat-app.onrender.com/](https://spring-chat-app.onrender.com/)**  
> Deployed using **Docker** on **Render**

---

✨ Features
- Real-time messaging with WebSocket + STOMP
- Auto-join user notifications
- Simple in-browser UI (HTML + JS)
- Dockerized for easy deployment

---

## 🛠 Tech Stack

- ⚙️ **Backend**: Spring Boot, WebSocket, STOMP
- 🐳 **Deployment**: Docker, Render
- 📦 **Build Tool**: Maven
- ☕ **Java** 17+

---

## 📦 Getting Started (Local Setup)

### Prerequisites

- Java 17+
- Maven
- Docker (for containerized deployment)

### 1. Clone the Repository
  ```bash
  git clone https://github.com/karanshah1561998/spring-chat-app.git
  cd spring-chat-app
  ```

### 2. Run Locally (Dev Mode)
  ```bash
  ./mvnw spring-boot:run
  ```
  Then open your browser at:📍 http://localhost:8080

### 3. Run via Docker
  ```bash
  ./mvnw clean package
  docker build -t spring-chat-app .
  docker run -p 8080:8080 spring-chat-app
  ```

### 📁 Project Structure
  ```bash
  src/
  ├── main/
  │   ├── java/com/project/chat/...
  │   └── resources/static/index.html  # Frontend UI
  ├── test/
  └── Dockerfile
  ```

📡 WebSocket Endpoints
  ```bash
  ws://localhost:8080/ws: WebSocket handshake endpoint
  
  Topics:
  /topic/public: Broadcast messages to all
  
  Destinations:
  /app/chat.sendMessage: Send a message
  /app/chat.addUser: Add new user
  ```
