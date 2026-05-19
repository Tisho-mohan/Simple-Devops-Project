# 🚀 Simple DevOps Project - CI/CD Dockerized Flask App on AWS EC2

## 📌 Overview
This project demonstrates a full DevOps workflow using a Flask application, Docker containerization, GitHub Actions CI/CD, and AWS EC2 deployment.

The goal of this project is to simulate a real-world production pipeline:

- Build application (Flask)
- Containerize using Docker
- Automate CI/CD using GitHub Actions
- Push Docker image to Docker Hub
- Deploy and run container on AWS EC2

---

## 🛠 Tech Stack
- Python (Flask)
- Docker
- GitHub Actions (CI/CD)
- AWS EC2 (Ubuntu)
- Linux
- Git & GitHub

---

## 📁 Project Structure
Simple-Devops-Project/
├── app.py
├── Dockerfile
├── requirements.txt
├── .github/workflows/ci.yml
├── README.md
└── images/
    ├── aws-instance-created.png
    ├── ssh-into-instance.png
    ├── docker-ps.png
    ├── docker-logs.png
    ├── security-group-ports.png
    └── website-public-access.png

---

## ⚙️ CI/CD PIPELINE FLOW
1. Developer pushes code to GitHub (main branch)
2. GitHub Actions workflow starts automatically
3. Docker image is built
4. Docker image is pushed to Docker Hub
5. EC2 server pulls latest image
6. Container is stopped and restarted automatically

---

## 🚀 LOCAL SETUP (RUN PROJECT LOCALLY)

Clone repository:
git clone https://github.com/Tisho-mohan/simple-devops-project.git
cd simple-devops-project

Build Docker image:
docker build -t myapp .

Run container:
docker run -d -p 5000:5000 --name flask-app myapp

Check running containers:
docker ps

View logs:
docker logs flask-app

Open in browser:
http://localhost:5000

---

## ☁️ AWS EC2 DEPLOYMENT

SSH into server:
ssh -i your-key.pem ubuntu@your-ec2-ip

Pull image from Docker Hub:
docker pull your-dockerhub-username/simple-devops-project:latest

Run container:
docker run -d -p 5000:5000 --name flask-app your-dockerhub-username/simple-devops-project:latest

Verify:
docker ps

---

## 🌐 SECURITY GROUP SETUP
- 22 → SSH access
- 5000 → Flask application access

---

## 🔗 LIVE APPLICATION
http://13.60.41.70:5000/

---

## 🎯 LEARNING OUTCOMES
- Docker containerization
- AWS EC2 deployment
- CI/CD automation using GitHub Actions
- Linux server management
- Cloud networking basics
- End-to-end DevOps pipeline

---

## 📌 FUTURE IMPROVEMENTS
- Add versioned Docker images (v1, v2, v3)
- Add Nginx reverse proxy
- Add monitoring (Prometheus + Grafana)
- Add Docker Compose setup
- Add staging and production environments
