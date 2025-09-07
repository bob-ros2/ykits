# ykit-fastapi - Micro Service Kit with health service

A minimal FastAPI microservice with health check and Docker Compose deployment.

## Features
- FastAPI service with `/health` endpoint
- Built with Docker and Docker Compose
- Health checks (60s interval) for service readiness

## Usage
1. Navigate into the project directoy
2. Run `docker compose up -d` to build and start the service as a deamon
3. To test if it is running send a GET request to http://localhost:8080/health If localhost is not reachable use the according ip address or hostname or servicename

## Force rebuild
After changes, a re-build can be forced by `docker compose up -d --force-recreate --build`

## Services
- Health endpoint at http://localhost:8080/health
- FastAPI - Swagger UI at http://localhost:8080/docs
- OpenAPI JSON at http://192.168.1.47:8080/openapi.json

## Contained Files
- Entrypoint: app.py
- Dockerfile
- compose.yaml
- README.md

