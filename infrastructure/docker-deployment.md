# Docker Deployment

This guide covers deploying services using Docker.

## Prerequisites

- Docker and Docker Compose installed
- Access to the container registry

## Building an Image

```bash
docker build -t my-app:latest .
```

## Running with Docker Compose

```bash
docker-compose up -d
```

## Pushing to Registry

```bash
docker tag my-app:latest registry.example.com/my-app:latest
docker push registry.example.com/my-app:latest
```

_Environment-specific deployment guides to be added._
