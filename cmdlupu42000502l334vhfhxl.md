---
title: "🚀 Day 8 of My AWS & DevOps Journey – Dockerfile + GitHub Repo + Project Push"
datePublished: Sun Jul 27 2025 15:46:04 GMT+0000 (Coordinated Universal Time)
cuid: cmdlupu42000502l334vhfhxl
slug: day-8-of-my-aws-and-devops-journey-dockerfile-github-repo-project-push
tags: cloud, learning, devops, success

---

Hey DevOps Learners! 👋

Today is Day 8 of my journey toward becoming a Cloud & DevOps Engineer, and it was a productive one! I focused on structuring a real project using Docker and pushing it to GitHub for the first time. 🚀

\---

📌 What I Did Today

🔹 1. Created My First Docker Project Repo

I created a GitHub repository for my Docker + Flask project:

Project: Flask app inside Docker container, deployed on EC2

Repo Name: flask-docker-app (public)

Added:

Dockerfile

app.py

requirements.txt

README.md

✅ This is now ready to be shown in resumes, interviews, and LinkedIn!

\---

🔹 2. Dockerfile Breakdown

I created a clean and simple Dockerfile:

FROM python:3.9-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt

COPY . .

CMD \["python", "app.py"\]

✅ This builds a lightweight container running a Python Flask app.

\---

🔹 3. Published Project to GitHub

Steps I followed:

1\. Initialized Git repo: git init

2\. Connected to GitHub:

git remote add origin https://github.com/Sukaran-233/flask-docker-app.git

3\. Added + committed files:

git add .

git commit -m "Initial commit"

4\. Pushed project:

git push -u origin main

🧠 Lesson: Keep your README file u

pdated. It helps recruiters and peers understand your project quickly!