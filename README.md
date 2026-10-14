# TP3 Middlewares Microservices

This folder contains a middleware-oriented microservice implementation with:

- gateway
- ms-registry
- ms-formation
- ms-scolarite

## Overview

It follows a classic Spring Cloud architecture:

- the registry handles service discovery
- the gateway acts as the entry point
- business services expose domain endpoints and communicate through the platform infrastructure

## Docker deployment

The project includes a docker-compose.yml file for local orchestration.

```bash
docker compose up --build
```

## Service ports

- Registry: 8888
- Gateway: 7777
- Formation: 8081
- Scolarite: 8080

## Local Maven run

Each service can be started separately with Maven:

```bash
cd ms-registry
./mvnw spring-boot:run
```

```bash
cd ../gateway
./mvnw spring-boot:run
```

```bash
cd ../ms-formation
./mvnw spring-boot:run
```

```bash
cd ../ms-scolarite
./mvnw spring-boot:run
```

## Purpose

This project is useful for practicing middleware concepts, routing, discovery, and container-based deployment in a microservice environment.
