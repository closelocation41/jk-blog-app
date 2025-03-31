# JK Blog App - Setup & Features Guide

## Prerequisites
Before setting up the project, ensure the following prerequisites are met:

- Create a **Google Auth Client** and generate secret keys.
- Install [MongoDB](https://www.mongodb.com/try/download/community).
- Create a `.env` file and copy all data from `example.env`.
- Update AWS secrets.
- Update Google authentication keys.
- **Generate dummy data** using the `dummy-data-generator` app:
  - Run `node app.js` or `node bulk-generator.js`.
  - Check the `static` folder and **code coverage screenshots**.

---

## Local Setup

### Clone the repositories
```sh
git clone https://github.com/closelocation41/jk-backend.git

git clone https://github.com/closelocation41/jk-frontend.git

git clone https://github.com/closelocation41/jk-blog-app.git
```

### 1) Local Setup Without Docker

#### Backend Setup (NestJS)
Navigate to the backend directory:
```sh
cd jk-backend
```
Install dependencies:
```sh
npm install
```
Create and configure `.env` file:
```sh
cp example.env .env
```
Start the development server:
```sh
npm run start:dev
```
Backend will be available at `http://localhost:3000`

#### Frontend Setup (Angular)
Navigate to the frontend directory:
```sh
cd ../jk-frontend
```
Install dependencies:
```sh
npm install
```
Start the development server:
```sh
npm run start
```
Frontend will be available at `http://localhost:4200`

Login with Google authentication.

---

### 2) Local Setup With Docker
Clone repositories:
```sh
git clone https://github.com/closelocation41/jk-backend.git

git clone https://github.com/closelocation41/jk-frontend.git

git clone https://github.com/closelocation41/jk-blog-app.git
```

Build the Docker images:
```sh
docker-compose build
```
Run Docker Compose:
```sh
docker-compose up -d
```
Ensure `docker-compose.yml` is correctly configured:
```sh
https://github.com/closelocation41/jk-blog-app
```

---

### 3) AWS ECR Setup

#### Create AWS ECR Repository
Create an ECR repository for `jk-backend` and `jk-frontend` in AWS.

#### Clone Repositories
```sh
git clone https://github.com/closelocation41/jk-backend.git

git clone https://github.com/closelocation41/jk-frontend.git

git clone https://github.com/closelocation41/jk-blog-app.git
```

#### Build and Push Images to AWS ECR
Build Docker images for `jk-backend` and `jk-frontend`, then push them to AWS ECR.

#### Setup EC2 Instance and Deploy GitHub Action Runner
- Create an **EC2 instance**.
- Deploy **self-hosted GitHub Action Runner**.
- Update **ECR repository URLs** in `docker-compose.yml`.
- Deploy GitHub workflow.

Create and configure `.env` file:
```sh
cp example.env .env
```

---

## Features Covered in JK Blog App

### Design & Architecture
- Well-structured **Class, API, and Database design** with clear explanations.
- Focus on **API performance, database integrity, and consistency**.
- Uses **Microservices Architecture** for scalability.
- Usage of **design patterns** for maintainability.

### Testing & Automation
- **95%+ test coverage** ensuring functionality, performance, and reliability.
- **Automated REST API testing** for robust backend validation.
- **Test data generation** for large-scale scenarios (e.g., 1000+ users, 100,000+ entities).
- Performance testing with a focus on scalability.

### Security & Authentication
- Integration with **Google Authentication**.
- Secure **Authentication & Authorization** implementation.
- Good understanding and implementation of **HTTP/HTTPS security, debugging, monitoring, and logging**.

### Database & ORM
- Uses **MongoDB with ORM** for optimized query execution.
- Demonstrates efficient **data modeling and large dataset handling**.
- Ensures **database integrity and consistency**.

### Frontend Development
- Written entirely in **TypeScript**.
- **Modular UI components** following design patterns.
- Well-documented and **simple, maintainable code**.
- **Responsive design** targeting multiple browsers and devices.
- **Google PageSpeed Insights** score of **90%+**.
- Integration with **website analytics** for performance tracking.
- **Web application test automation** for functional validation.

### Backend Development
- Written entirely in **TypeScript**.
- Demonstrates strong **Object-Oriented Programming (OOP) skills**.
- **Automated API testing** ensuring reliability.
- Large-scale **test data generation** and database management.
- **Microservices-based backend** for scalability.
- **Problem-solving approach** to real-world scenarios.

### Deployment & Scalability
- **AWS ECR & EC2 Deployment** with self-hosted GitHub Action Runner.
- **Dockerized microservices** for easy deployment and scalability.
- Designed to handle **millions of users efficiently**.

---

Now your project is set up for local development and AWS deployment! 🚀

