# DevOps Assignment – Dockerize and Deploy a Web App on AWS EC2

This project demonstrates a simple Node.js web app that is containerized using Docker and deployed on an AWS EC2 instance using DevOps principles.


## Tech Stack

- Node.js (Express)
- Docker
- AWS EC2 (Ubuntu 22.04)

---
## ✅ Project Structure

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

## Deploy on AWS EC2

### 1. Launch EC2 Instance

- OS: Ubuntu 22.04  
- Type: t2.micro  
- Security Group: Open port 3000  
- Key Pair: simple-node-app.pem

![Screenshot 2025-06-26 185647](https://github.com/user-attachments/assets/c2dcc389-58c8-4a7b-9cc4-df9c09093bad)
EC2 Dashboard


### 2. Connect via SSH
public ip in this case is 13.236.86.91
```bash
ssh -i "simple-node-app.pem" ubuntu@13.236.86.91
```

### 3. Install Docker & Git
```bash
sudo apt update
sudo apt install docker.io git -y
```
### 4. Clone Repository on EC2
```bash
git clone https://github.com/PrateekMahadev/simple-node-app.git
cd simple-node-app
```
### 5. Build and Run Docker Container
```bash
sudo docker build -t simple-node-app .
sudo docker run -d -p 3000:3000 simple-node-app
```
Docker running app on EC2:
![Screenshot 2025-06-27 155715](https://github.com/user-attachments/assets/7189b40e-18a0-4cb0-9d8d-bdd14397182a)


### 6. Test in Browser

Visit: `http://<EC2-PUBLIC-IP>:3000`

Expected output:
![Screenshot 2025-06-26 211536](https://github.com/user-attachments/assets/4b2e766d-5220-4398-93fd-f2740fddaa3f)
App accessible from public ip

## Summary

- Dockerized a Node.js web app  
- Deployed and ran it successfully on AWS EC2  
- Documented steps and screenshots as requested

---

## Thank You!

