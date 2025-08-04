# FastAPI Hello World Project

A simple FastAPI application with Docker support.

## Features

- Basic FastAPI application with Hello World endpoint
- Health check endpoint
- Items endpoint with path and query parameters
- Docker containerization

## Local Development

### Prerequisites

- Python 3.11+
- pip

### Setup

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Run the application:
```bash
uvicorn main:app --reload
```

The API will be available at `http://localhost:8000`

### API Documentation

FastAPI automatically generates interactive API documentation:
- Swagger UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`

## Docker

### Build the Docker image

```bash
docker build -t fastapi-hello-world .
```

### Run the Docker container

```bash
docker run -p 8000:8000 fastapi-hello-world
```

The application will be available at `http://localhost:8000`

## Endpoints

- `GET /` - Hello World message
- `GET /health` - Health check
- `GET /items/{item_id}` - Get item by ID with optional query parameter
