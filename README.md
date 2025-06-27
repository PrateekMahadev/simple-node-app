# DevOps Assignment – Dockerize and Deploy a Web App on AWS EC2

This project demonstrates a simple Node.js web app that is containerized using Docker and deployed on an AWS EC2 instance using DevOps principles.

---

## GitHub Repository

[https://github.com/PrateekMahadev/simple-node-app](https://github.com/PrateekMahadev/simple-node-app)

---

## Tech Stack

- Node.js (Express)
- Docker
- AWS EC2 (Ubuntu 22.04)

---

## Project Structure

simple-node-app/
├── app.js
├── Dockerfile
├── .dockerignore
├── package.json
├── package-lock.json


## Run Locally Using Docker

### 1. Clone the Repository
```bash
git clone https://github.com/PrateekMahadev/simple-node-app.git
cd simple-node-app
```

### 2. Build the Docker Image
```bash
docker build -t simple-node-app .
```

### 3. Run the App
```bash
docker run -p 3000:3000 simple-node-app
```

### 4. Open in Browser

Visit: `http://localhost:3000`

You should see:
![Screenshot 2025-06-26 172820](https://github.com/user-attachments/assets/2c1ec333-ac13-46e0-a6ee-7b7b8a10382e)
App running locally on Docker



