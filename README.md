# 💬 Spring Boot Chat App
A real-time chat application built with **Spring Boot**, **WebSockets**, and **STOMP messaging protocol**. This project demonstrates how to build a scalable backend with real-time communication. Users can exchange messages instantly through a WebSocket connection.

## 🚀 Live Demo
Access the live app here: [Spring Boot Chat App](https://spring-chat-app.onrender.com)

## ✨ Features
- Real-time messaging with WebSocket + STOMP
- Join Notifications for New Users
- Simple Frontend UI (Vanilla JS + HTML)
- Dockerized for easy deployment

## 🛠 Tech Stack
- Backend: Spring Boot, WebSocket, STOMP
- Deployment: Docker, Render
- Build Tool: Maven
- Java 17+

## ⚙️ Installation
### Prerequisites
**Ensure you have the following installed:**
- Java 17+
- Maven
- Docker (for containerized deployment)

### Setup
1. **Clone the Repository**
   ```bash
   git clone https://github.com/karanshah1561998/spring-chat-app.git
   cd spring-chat-app

2. **Run Locally (Dev Mode)**
   ```bash
   ./mvnw spring-boot:run
   Then open your browser at:📍 http://localhost:8080

3. **Run with Docker**
   ```bash
   ./mvnw clean package
   docker build -t spring-chat-app .
   docker run -p 8080:8080 spring-chat-app

## 🧩 Troubleshooting

### 1. WebSocket Not Connecting
- Ensure the WebSocket endpoint in your frontend matches the backend (`ws://localhost:8080/ws`).
- Check browser console for CORS or STOMP errors.

### 2. Port 8080 Already in Use
- Another service might be using port 8080.
- Either kill the conflicting process or change the server port in `application.properties`.

### 3. Docker Image Build Fails
- Make sure you've run `./mvnw clean package` before building the Docker image.
- Verify Docker is running and accessible from your terminal.

### 4. Frontend Not Loading
- Ensure `index.html` is present in the `resources/static/` directory.
- Check if Spring Boot is correctly serving static resources.

### 5. Messages Not Being Broadcasted
- Confirm STOMP endpoints and destinations are correctly mapped.
- Check backend logs for any message mapping or subscription errors.
