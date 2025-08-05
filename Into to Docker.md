# TryHackMe: Intro to Docker

**Author:** Harry  
**Platform:** TryHackMe  
**Room:** Intro to Docker  
**Difficulty:** Easy  
**Tags:** Docker, Containers, Linux

---

## 🧠 Introduction

This room introduces the fundamentals of Docker, including how containers work, Dockerfile basics, Docker Compose, and practical container management. It is ideal for beginners who have a basic understanding of Linux. The tasks guide you through core concepts and commands you’ll need for real-world container use.

This write-up is prepared by me as part of my TryHackMe learning journey.

---

## 📘 Task 1: Introduction

> **Answer:** No answer needed.

---

## 🧱 Task 2: Basic Docker Syntax

1. **Pull a Docker image**
   - `docker pull`
2. **List all images**
   - `docker image ls`
3. **Pull the image "tryhackme"**
   - `docker pull tryhackme`
4. **Pull the image "tryhackme" with tag "1337"**
   - `docker pull tryhackme:1337`

---

## 🐳 Task 3: Running Your First Container

1. **Run container interactively**
   - `docker run -it`
2. **Run container in detached mode**
   - `docker run -d`
3. **Run container and bind to port 80**
   - `docker run -p 80:80`
4. **List running containers**
   - `docker ps`
5. **List all containers (including stopped)**
   - `docker ps -a`

---

## 📦 Task 4: Intro to Dockerfiles

1. **Specify base image**
   - `FROM`
2. **Run a command inside container**
   - `RUN`
3. **Build image using Dockerfile**
   - `build`
4. **Name/tag the image**
   - `-t`

---

## ⚙️ Task 5: Intro to Docker Compose

1. **Start containers**
   - `up`
2. **Delete containers**
   - `down`
3. **Compose file name**
   - `docker-compose.yml`

---

## 🧠 Task 6: Intro to the Docker Socket

1. **IPC stands for**
   - `Interprocess Communication`
2. **Docker server is equivalent to**
   - `API`

---

## 🛠️ Task 7: Practical

1. **Running container name**
   - `CloudIsland`
2. **Flag from starting webserver**
   - `THM{WEBSERVER_CONTAINER}`

---

## ✅ Conclusion

This room gives a solid foundation to Docker and container-based environments. Understanding these tools is essential in DevOps, cybersecurity labs, and software development.
