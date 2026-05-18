# Simple DevOps Project - Dockerized Flask App

## Overview
This is my first DevOps learning project where I built a simple Python Flask application and containerized it using Docker.

The goal of this project is to understand basic DevOps workflow:
- Writing application code
- Containerizing with Docker
- Using Git & GitHub for version control

## Tech Stack
- Python (Flask)
- Docker
- Git & GitHub
- Linux (Fedora)

## Project Structure

Simple-Devops-Project/
├── app.py
├── Dockerfile
├── requirements.txt
└── README.md

## How It Works
1. Flask app runs a simple web server
2. Docker builds the application into a container
3. Container runs on port 5000

## Run Locally

### 1. Clone repo (Linux)
git clone https://github.com/Tisho-mohan/simple-devops-project.git
cd simple-devops-project

## Build Docker image
docker build -t myapp .

## Run container
docker run -d -p 5000:5000 myapp

## Open in Browser
http://localhost:5000
