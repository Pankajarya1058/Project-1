# Dockerized Node.js Application with CI/CD using GitHub Actions

## Overview

This project demonstrates a basic Node.js application containerized with Docker and integrated with a CI/CD pipeline using GitHub Actions. The application is automatically tested and pushed to Docker Hub upon every commit to the `main` branch.

## Features

- Node.js and Express server
- Unit testing using Jest
- Dockerfile for containerization
- GitHub Actions workflow for CI/CD
- Automated Docker image build and push to Docker Hub

## Prerequisites

- Node.js and npm
- Docker installed and running
- Docker Hub account
- GitHub repository with Actions enabled

## Project Structure

project-root/
├── app.js 
├── package.json 
├── Dockerfile 
├── .github/workflows/ 
│           └── ci.yml 
└── test/ 
      └── sample.test.js

## Getting Started

### 1. Clone the repository
```
git clone https://github.com/Pankajarya1058/Project-1.git
cd Project-1
```

### 2. Install dependencies
```
npm install
```

### 3. Run the application locally
```
npm start
```
```
Navigate to http://localhost:3000 to see the app.
```

### 4. Run tests
```
npm test
```

## Docker Setup

### Build the Docker image
```
docker build -t your-dockerhub-username/my-app .
```

### Run the Docker container
```
docker run -d -p 3000:3000 your-dockerhub-username/my-app

# example:- To check this node application run below command
# docker run -d -p 3000:3000 pankajarya12345/my-app:latest
```

### GitHub Actions CI/CD

This project uses GitHub Actions to:
- Install Node.js and dependencies
- Run tests
- Build the Docker image
- Log in to Docker Hub
- Push the Docker image

### Setup Secrets

In your GitHub repository settings, configure the following secrets:
```
DOCKER_USERNAME – your Docker Hub username
DOCKER_PASSWORD – your Docker Hub password
```


