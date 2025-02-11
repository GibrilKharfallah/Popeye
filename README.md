# 🗳️ Popeye - Dockerized Voting App

## 📖 Overview
This is a **containerized web application** that allows users to vote between two options and view real-time results.  
The project follows a **microservices architecture** and runs using **Docker and Docker Compose**.

## ⚙️ Technologies Used
- **Docker & Docker Compose** – Containerization and orchestration  
- **Python (Flask)** – Voting service (`poll`)  
- **Redis** – Message queue for temporary vote storage  
- **Java (Maven, OpenJDK)** – Worker service (`worker`) that processes votes  
- **PostgreSQL** – Database for persistent vote storage  
- **Node.js (Express.js)** – Result service (`result`) for displaying votes  

## 🏗️ Project Architecture
The application consists of five main services:

| Service  | Technology | Description |
|----------|-----------|-------------|
| **Poll** | Python (Flask) | Collects votes and sends them to Redis |
| **Redis** | Redis | Temporary queue for votes |
| **Worker** | Java (Maven) | Processes votes from Redis and saves them to PostgreSQL |
| **Database** | PostgreSQL | Stores votes persistently |
| **Result** | Node.js (Express) | Displays voting results |
