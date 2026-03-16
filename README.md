# Containerized Web Application with PostgreSQL using Docker Compose and Macvlan/Ipvlan

This project demonstrates containerization using Docker and Docker Compose.

## Technologies Used

- FastAPI
- PostgreSQL
- Docker
- Docker Compose

## Project Structure

```
container-project
│
├── backend
│   ├── main.py
│   └── Dockerfile
│
├── database
│   └── Dockerfile
│
├── docker-compose.yml
└── README.md
```

## Run the Project

```bash
docker compose up --build
```

## API Endpoints

Health Check

```
/health
```

Insert Data

```
/insert
```

Fetch Data

```
/fetch
```

## Networking

Containers communicate using Docker internal networking.

## Persistence

PostgreSQL data is stored in Docker volumes.
