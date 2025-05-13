# 🗳️ ComposeMonVote

**ComposeMonVote** is a containerized web application designed for managing and visualizing polls in real-time. The system consists of multiple services communicating together using Docker and Docker Compose.

## ⚙️ Overview

The app allows users to vote in a poll, processes those votes asynchronously, and displays the results live. The architecture follows a microservices approach using Docker.

## 🧩 Architecture

The project is composed of **5 services**:

| Service | Description |
|--------|-------------|
| `poll`   | Web frontend where users can cast votes |
| `result` | Web interface to display real-time results |
| `worker` | Background processor that listens for votes and updates results |
| `redis`  | Message broker used for temporary vote storage |
| `db`     | Relational database to persist poll and result data |

## 🐳 Docker Setup

### ✅ Prerequisites

- Docker
- Docker Compose

### 🚀 Run the App

```bash
docker-compose up --build -d
```

## 🌐 Access the App

Vote (poll): http://localhost:5000

Result (result): http://localhost:5001

## ⚙️ Service Ports

| Service | Port                     |
| ------- | ------------------------ |
| poll    | 5000                     |
| result  | 5001                     |
| worker  | N/A (runs in background) |
| redis   | 6379                     |
| db      | 5432                     |

## 📦 Environment Variables

Environment variables can be defined in each service to configure DB connection strings, Redis hosts, etc.  
Currently, the environment variables are basic. (POSTGRES_USER = myuser, POSTGRES_PASSWORD = mypassword)

## 📄 License

This project is licensed under the MIT License.
See the LICENSE file for details.



