# Docker Assignment - Node.js Frontend and Flask Backend

## Overview

This project demonstrates communication between a Node.js (Express) frontend and a Flask backend using Docker and Docker Compose.

The frontend provides a web form that collects user information and sends it to the Flask backend. The backend processes the submitted data and returns a response to the frontend.

---

## Technologies Used

* Node.js
* Express.js
* Flask
* Docker
* Docker Compose
* Git & GitHub

---

## Project Structure

```text
docker-assignment/
│
├── frontend/
│   ├── views/
│   │   └── index.ejs
│   ├── app.js
│   ├── package.json
│   └── Dockerfile
│
├── backend/
│   ├── app.py
│   ├── requirements.txt
│   └── Dockerfile
│
├── docker-compose.yml
└── .gitignore
```

---

## Features

* Express frontend with HTML form
* Flask backend API
* Communication between frontend and backend containers
* Dockerized services
* Docker Compose networking
* GitHub version control
* Docker Hub image publishing

---

## Frontend

The frontend is developed using Express.js and EJS templates.

### Routes

* `GET /`

  * Displays the form.

* `POST /submit`

  * Sends form data to the Flask backend.

### Port

```text
3000
```

---

## Backend

The backend is developed using Flask.

### API Endpoint

#### POST /submit

Accepts JSON data:

```json
{
  "name": "John",
  "email": "john@example.com"
}
```

Returns:

```json
{
  "message": "Data received successfully",
  "name": "John",
  "email": "john@example.com"
}
```

### Port

```text
5000
```

---

## Docker Setup

### Build Containers

```bash
docker compose build
```

### Run Containers

```bash
docker compose up
```

### Stop Containers

```bash
docker compose down
```

---

## Docker Compose Services

### Frontend

* Container Name: node_frontend
* Port: 3000

### Backend

* Container Name: flask_backend
* Port: 5000

---

## Access Application

Open browser:

```text
http://localhost:3000
```

Fill out the form and submit.

---

## Docker Hub Images

### Frontend Image

```text
docker push <dockerhub-username>/node-frontend:latest
```

### Backend Image

```text
docker push <dockerhub-username>/flask-backend:latest
```

---

## GitHub Repository

Clone Repository:

```bash
git clone https://github.com/<username>/<repository-name>.git
```

---

## Screenshots Included

* Project Structure
* Docker Build Output
* Docker Compose Execution
* Browser Output
* Docker Hub Repositories
* GitHub Repository

---

## Author

Mohit

CDAC Docker Assignment
