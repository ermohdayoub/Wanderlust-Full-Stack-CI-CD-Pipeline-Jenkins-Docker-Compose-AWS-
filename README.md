# 🌍 Wanderlust – Full-Stack CI/CD Pipeline (Jenkins + Docker + Compose + AWS)

<p align="center">
  <img src="https://img.shields.io/badge/DevOps-CI%2FCD-blue" />
  <img src="https://img.shields.io/badge/Docker-Containers-brightgreen" />
  <img src="https://img.shields.io/badge/Jenkins-Automation-red" />
  <img src="https://img.shields.io/badge/AWS-EC2-orange" />
  <img src="https://img.shields.io/badge/Node.js-Backend-success" />
  <img src="https://img.shields.io/badge/MongoDB-Database-green" />
</p>

<img width="1919" height="1008" alt="Screenshot 2025-11-20 194118" src="https://github.com/user-attachments/assets/25164d6f-ad41-49e5-b586-138bd9ace337" />


## 📌 Overview

A complete **production-ready DevOps pipeline** for a travel booking application built with **Node.js, React, MongoDB** and automated through **Jenkins CI/CD**. The entire stack is containerized using **Docker & Docker Compose** and deployed on **AWS EC2**.

This project demonstrates real DevOps concepts: CI/CD, containerization, multi-container orchestration, pipeline automation, and cloud deployment.

---

## 🏗️ Architecture Diagram

```
            ┌────────────────────────────────────┐
            │             GitHub Repo             │
            └────────────────────────────────────┘
                           │ (Webhook/Pull)
                           ▼
┌────────────────────────────────────────────────────────────┐
│                         Jenkins CI/CD                      │
│  (Clone → Build → Test → Docker Compose Deploy)            │
└────────────────────────────────────────────────────────────┘
                           │
                           ▼
             ┌─────────────────────────┐
             │       AWS EC2           │
             ├─────────────────────────┤
             │  Docker Compose Stack   │
             │  - Backend (Node.js)    │
             │  - Frontend (React)     │
             │  - MongoDB Database     │
             └─────────────────────────┘
                           │
                           ▼
              User Access → http://EC2-IP:5173
```

---

## 🚀 Features

* **Automated CI/CD** using Jenkins Pipeline
* **Multi-container deployment** using Docker Compose
* **Node.js Backend + MongoDB Database** with persistent volumes
* **React Frontend build** using production-ready Node image
* Automated build caching & cleanup to avoid disk full errors
* **MongoDB DNS error fix** and container health checks
* **Environment variable support** (`.env.docker` → `.env` inside container)
* AWS EC2 deployment

---

## 🧰 Tech Stack

| Layer         | Technology                     |
| ------------- | ------------------------------ |
| Frontend      | React, Node.js Build Tools     |
| Backend       | Node.js, Express.js            |
| Database      | MongoDB (Dockerized)           |
| CI/CD         | Jenkins (Pipeline + Agent)     |
| Orchestration | Docker, Docker Compose         |
| Cloud         | AWS EC2 (Ubuntu)               |
| Others        | Linux, GitHub, Shell Scripting |

---

## 🐳 Docker Compose Setup

### Start Application

```
docker-compose up -d --build
```

### Stop Application

```
docker-compose down
```

This launches:

* **Node.js backend** 
* **React frontend** 
* **MongoDB** container with persistent volume `ci-cd_data`

---

## 🔧 Jenkins CI/CD Pipeline

### Pipeline Stages

1. **Clone Code** from GitHub
2. **Docker Compose Build** (frontend + backend)
3. **Docker Compose Deploy**

### Example Jenkinsfile


<img width="1919" height="1011" alt="Screenshot 2025-11-20 194400" src="https://github.com/user-attachments/assets/11347731-30f8-4da4-9bdb-700bee895df6" />
<img width="1919" height="1015" alt="Screenshot 2025-11-20 194416" src="https://github.com/user-attachments/assets/0a384cbb-940b-4b77-babf-e3aab1d837ab" />


## 🛠 Backend (Node.js) – Metrics Ready

* Production-ready `npm start` replaced nodemon
* Multi-stage Dockerfile for optimized image
* Exposed metrics endpoint possible using `prom-client`

screenshots of the project
<img width="1919" height="883" alt="Screenshot 2025-11-20 194453" src="https://github.com/user-attachments/assets/fc6f13b6-5cc0-45b1-a993-6237af3c86f9" />
<img width="1912" height="896" alt="Screenshot 2025-11-20 194718" src="https://github.com/user-attachments/assets/f9645639-8881-4b0a-84ed-d8984a58a1ba" />
<img width="1919" height="838" alt="Screenshot 2025-11-20 194247" src="https://github.com/user-attachments/assets/def38554-d446-4846-bb1c-20dafff5c4c2" />
<img width="1917" height="890" alt="Screenshot 2025-11-20 194614" src="https://github.com/user-attachments/assets/822ba24e-cd9b-445b-b099-768b4fc63fc1" />
<img width="1919" height="1016" alt="Screenshot 2025-11-20 194212" src="https://github.com/user-attachments/assets/d0e1fc1b-cff9-47ee-9c66-d11b866bd43a" />
<img width="1919" height="1016" alt="Screenshot 2025-11-20 194142" src="https://github.com/user-attachments/assets/24ae8ced-8ab7-495f-b25a-6bba0ef7ad0d" />
<img width="437" height="202" alt="Screenshot 2025-11-20 194104" src="https://github.com/user-attachments/assets/1e8c4d26-5f3e-440c-b8f0-011f6e1cf9e8" />
<img width="1919" height="838" alt="Screenshot 2025-11-20 194247" src="https://github.com/user-attachments/assets/0584bd44-a3bb-4900-8a53-d906a8b160b9" />
## ⭐ Results


* Fully automated CI/CD pipeline
* Zero manual steps after code commit
* Reproducible deployments using Docker Compose
* MongoDB + Node.js environment fully isolated
* Scalable & production-ready architecture

---

## ⭐ If you like this project

Please **star** ⭐ this repository — it helps a lot!
