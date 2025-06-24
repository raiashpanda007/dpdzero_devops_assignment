# 🧪 DevOps Assignment: Nginx Reverse Proxy + Docker Compose

This project demonstrates a reverse proxy setup using Docker Compose. It consists of:

- Two simple backend services:
  - **service_1**: built with Go
  - **service_2**: built with Python (Flask)
- One **Nginx container** acting as a reverse proxy, routing based on URL paths.

---

## 🧱 Tech Stack

- Docker + Docker Compose
- Go (for service_1)
- Python + Flask (for service_2)
- Nginx

---

## ⚙️ How to Run

Clone the repo:

```bash
git clone https://github.com/raiashpanda007/dpdzero_devops_assignment.git
cd dpdzero_devops_assignment
docker-compose up --build
