# Git and Docker Starter Application

This repository contains a small Python web application used to practice Git, GitHub, and Docker workflows.

## Application

The application listens on port 8000 and returns a text response when accessed over HTTP.

## Verification

The running application should be verified using an HTTP request to port 8000.
## Usage

Build the Docker image:

```bash
docker build -t git-docker-app:test .
```

Start the application with host port 8080 mapped to application port 8000:

```bash
docker run -d --name app-test -p 8080:8000 git-docker-app:test
```

Verify the response:

```bash
curl http://localhost:8080
```

The response includes a welcome message, service readiness, and
`Status: healthy - mannguyen2`.

View logs:

```bash
docker logs app-test
```

Stop and remove the container:

```bash
docker stop app-test
docker rm app-test
```
