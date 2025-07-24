# Express with Nginx Reverse Proxy - Dockerized Setup

This repository demonstrates how to containerize an Express.js application and serve it behind an Nginx reverse proxy using Docker and Docker Compose.

---

## Features

- **Express.js** backend application
- **Nginx** as a reverse proxy to handle client requests
- Containerized using **Docker**
- Multi-container orchestration via **Docker Compose**
- Easy setup and deployment

---

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/) installed
- [Docker Compose](https://docs.docker.com/compose/install/) installed

---

## Getting Started

1. **Clone the repository**

```bash
git clone https://github.com/your-username/express-nginx-docker.git
cd express-nginx-docker
```

2. **Build and start the containers**

```bash
docker-compose up --build
```

3. **Access the application**
-Open your browser and navigate to: http://localhost
Nginx will forward requests to the Express app running inside the container



## Project Structure 
```bash
.
├── docker-compose.yml
├── nginx
│   └── default.conf          # Nginx reverse proxy configuration
├── express-app
│   ├── Dockerfile            # Dockerfile for Express app
│   ├── package.json
│   └── index.js              # Express server code
└── README.md
```


## How It Works 
- Nginx listens on port 80 on the host machine.

- Requests to Nginx are forwarded to the Express app container.

- Express app listens on port 3000 inside its container.

- ocker Compose manages network and dependencies between containers.


## Customization 
- Modify nginx/default.conf to change proxy rules or add SSL termination.

- Update the Express app code in the express-app folder as needed.

- Change port mappings in docker-compose.yml for custom setups.



## Cleanup 
To stop and remove containers, networks, and volumes created by Docker Compose:

```
docker-compose down
```

## Additinoal resources :
  
https://hub.docker.com/repository/docker/rdip01/express-application-deployment

https://github.com/Dip-Barua/express-application-deployment-with-docker


