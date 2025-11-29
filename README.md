# 🤖 MNIST Neural Network Playground
*Interactive web interface for training neural networks on MNIST dataset using Keras (Django backend) and React frontend*

> **Note:**
> For the frontend to function correctly, you must configure the MNIST Web Backend project.  
> To configure the backend, go to [MNIST Web Backend](https://github.com/shaitansix/Mnist_Web-Backend).

---
## 🚀 Quick Setup Guide

## Using docker

### 1. Download the Docker Hub image
```bash
docker pull shaitansix/mnist_web-client:1
```

### 2. Create a Docker container and then initialize it
```bash
docker run --name mnist_web-client -e VITE_API_URL=http://localhost:8000 -p 5173:5173 shaitansix/mnist_web-client:1
```

*✔️ Frontend available at: 
http://localhost:5173/*

## Using Node Js

### 1. Create a folder for the project and open cmd in this folder

### 2. Clone the Repository
```bash
git clone https://github.com/shaitansix/Mnist_Web-Frontend.git
cd Mnist_Web-Frontend
```

### 3. Install dependencies
```bash
npm install
```

### 4. Configure environment variables:
**Create an .env.development file in the Mnist_Web-Frontend folder**
```bash
VITE_API_URL=http://localhost:8000
```

### 4. Run the development server
```bash
npm run dev
```

*✔️ Frontend available at: 
http://localhost:5173/*