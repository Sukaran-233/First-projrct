---
title: "📅 Day 7: Docker Distroless Image + Flask App Deployment (Hands-On)"
datePublished: Sat Jul 26 2025 18:40:38 GMT+0000 (Coordinated Universal Time)
cuid: cmdklihua000c02l81ef2bcqi
slug: day-7-docker-distroless-image-flask-app-deployment-hands-on
tags: docker, devops, distroless

---

Today’s goal was to go deeper into Docker by working with Distroless images and deploying a small Flask web app using a custom Dockerfile.

\---

🚀 What I Learned

✅ What Are Distroless Images?

Distroless images are minimal Docker images without a full Linux distribution.

They contain only the application and its runtime, nothing more.

Why use them?

Smaller image size (faster pull/push)

Improved security (reduced attack surface)

Better performance

🧪 Real-World Example:

Imagine you're building a banking microservice where security is a top priority. A distroless image ensures there’s no shell access or package manager, reducing risk.

\---

🔧 Project: Flask App in Distroless Docker Image

Step-by-step:

1\. Create a Flask App (app.py)

from flask import Flask

app = Flask(\_\_name\_\_)

@app.route("/")

def home():

return "Hello from Distroless Flask!"

if \_\_name\_\_ == "\_\_main\_\_":

app.run(host="0.0.0.0", port=5000)

2\. Requirements File

Flask==2.3.2

3\. Dockerfile (Multi-stage build using Distroless)

\# Stage 1: Builder

FROM python:3.10-slim as builder

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

\# Stage 2: Distroless runtime

FROM gcr.io/distroless/python3

WORKDIR /app

COPY --from=builder /app /app

CMD \["app.py"\]

4\. Build & Run Docker

docker build -t flask-distroless .

docker run -p 5000:5000 flask-distroless

5\. Access the app

Open your browser: http://localhost:5000

\---

🧠 What I Understood Clearly

Difference between \_\_name\_\_ and \_\_main\_\_

Multi-stage Docker builds

How to access apps running inside containers

Security benefits of distroless images

\---

📌 Challenges I Faced

Typing \_\_name\_\_ correctly with underscores 😅

Error due to case-sensitive From in Dockerfile (FROM is correct)

Ensuring proper file structure while copying in multi-stage build

\---

🔄 Tomorrow’s Plan

Push this project to GitHub

Connect this Docker container to an NGINX reverse proxy

Start experimenting with Ansible playbooks

\---

🙌 Stay Connected

I’m documenting this journey daily — follow along and let’s grow together in Cloud + DevOps!

📍Hashnode: DevOpsWithSukaran

🔗 GitHub: github.com/Sukaran-233

💼 LinkedIn: mahajansukran