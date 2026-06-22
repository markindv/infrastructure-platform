Infrastructure Platform

A containerized infrastructure platform built with Docker Compose.

The project includes an Nginx web server and PostgreSQL database service with persistent storage, environment-based configuration, and isolated service networking.

Architecture

Client
  |
  v
Nginx Container
  |
  v
PostgreSQL Container
  |
  v
Docker Volume

Stack

* Docker
* Docker Compose
* Nginx
* PostgreSQL 17
* Docker Volumes
* Docker Networks
* Environment Variables
* Linux

Services

Nginx

* Serves static web content.
* Exposes port 8080 on the host.
* Mounts local index.html into the container.

PostgreSQL

* Runs PostgreSQL 17.
* Uses environment variables from .env.
* Stores database files in a persistent Docker Volume.
* Keeps data available after container recreation.

Project Structure

compose/
├── docker-compose.yml
├── .env
├── .gitignore
├── README.md
└── index.html

Environment Variables

The PostgreSQL service is configured using a .env file.

Example:

POSTGRES_DB=devops_db
POSTGRES_USER=devops_user
POSTGRES_PASSWORD=********

The .env file is excluded from Git using .gitignore.

Start Services

docker-compose up -d

Check Running Containers

docker ps

Expected services:

compose_nginx
compose_postgres

Open Web Server

http://localhost:8080

Connect to PostgreSQL

docker exec -it compose_postgres bash
psql -U devops_user -d devops_db

Stop Services

docker-compose down

Validation

The following scenarios were tested:

* Multi-container deployment with Docker Compose
* Automatic Docker Network creation
* Service communication inside the Compose network
* PostgreSQL configuration through environment variables
* Persistent database storage using Docker Volume
* Data persistence after container recreation

Database Persistence Test

A PostgreSQL table was created and populated with test data.

After running:

docker-compose down
docker-compose up -d

the data remained available, confirming that PostgreSQL data is stored in a Docker Volume rather than inside the container filesystem.

Author

Dmitry Markin

