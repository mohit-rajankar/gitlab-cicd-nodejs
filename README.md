# 🚀 Node.js Todo App with GitLab CI/CD Pipeline

A Dockerized Node.js Todo application deployed using a complete **GitLab CI/CD automation pipeline**.

This project focuses on DevOps practices:
- Automated build
- Testing stage
- Docker image creation
- Docker Hub image push
- Automated deployment using Docker Compose
- Self-hosted GitLab Runner on AWS EC2

---

## 📌 Project Overview

This project demonstrates a complete CI/CD workflow where every code push automatically triggers a pipeline.

Developer workflow:

```
Code Change
     |
     ↓
Git Push
     |
     ↓
GitLab CI/CD Pipeline
     |
     ├── Build Docker Image
     |
     ├── Run Tests
     |
     ├── Push Image to Docker Hub
     |
     └── Deploy Application
             |
             ↓
          AWS EC2
             |
             ↓
       Running Application
```

---

# 🛠️ Technologies Used

- Node.js
- Express.js
- EJS
- Docker
- Docker Compose
- GitLab CI/CD
- GitLab Self-Hosted Runner
- Docker Hub
- AWS EC2
- Linux

---

# 🏗️ Application Architecture

```
                Developer

                    |
                    |
                git push

                    ↓

              GitLab Repository

                    |
                    ↓

              GitLab Pipeline

        ┌───────────┼───────────┐
        ↓           ↓           ↓

      Build       Test       Push Image

        ↓                       ↓

   Docker Image          Docker Hub

                    ↓

              Deploy Stage

                    ↓

              AWS EC2 Server

                    ↓

            Docker Container

                    ↓

             Web Application
```

---

# 🔄 CI/CD Pipeline Stages

## 1. Build Stage

Creates a Docker image of the application.

Command:

```bash
docker build -t node-app:latest .
```

---

## 2. Test Stage

Runs application testing.

Example:

```bash
echo "testing..."
```

---

## 3. Push Stage

Logs into Docker Hub and pushes the latest image.

Process:

```
Docker Image

      ↓

Tag Image

      ↓

Push to Docker Hub
```

---

## 4. Deploy Stage

Deploys the latest application version using Docker Compose.

```bash
docker compose up -d
```

---

# 🐳 Docker Setup

The application is containerized using Docker.

Build image:

```bash
docker build -t node-app .
```

Run container:

```bash
docker run -p 8000:8000 node-app
```

---

# 🐋 Docker Compose

Docker Compose manages application deployment.

Start application:

```bash
docker compose up -d
```

Stop application:

```bash
docker compose down
```

---

# 📂 Project Structure

```
.
├── app.js
├── test.js
├── package.json
├── package-lock.json
│
├── Dockerfile
├── docker-compose.yml
├── .gitlab-ci.yml
├── .gitignore
│
├── views
│   ├── todo.ejs
│   └── edititem.ejs
│
└── README.md
```

---

# ⚙️ GitLab Runner

A self-hosted GitLab Runner is configured on AWS EC2.

The runner automatically executes pipeline jobs:

```
GitLab

   ↓

Runner

   ↓

Docker Commands

   ↓

Deployment
```

---

# 🌐 Deployment

Application runs inside a Docker container on AWS EC2.

Check running containers:

```bash
docker ps
```

View logs:

```bash
docker logs <container_id>
```

---

# 📸 Screenshots

## GitLab Pipeline

(screenshots/gitlab_pipeline.png)

---

## GitLab Runner

(screenshots/runner.png)

---

## Running Application

(screenshots/webapp)

---

#  Features Demonstrated

✅ CI/CD automation  
✅ Docker containerization  
✅ GitLab Runner configuration  
✅ Docker Hub integration  
✅ AWS EC2 deployment  
✅ Automated deployment workflow  

---

#  Future Improvements

- Add Nginx reverse proxy
- Add HTTPS with SSL
- Add Kubernetes deployment
- Add Terraform infrastructure
- Add Prometheus & Grafana monitoring

---

#  Author

Mohit Rajankar
