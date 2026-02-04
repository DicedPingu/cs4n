# Docker — containerized environments
# Use it to run apps in isolated, reproducible images.

## 1) Images
- `docker pull <image>` — download image
- `docker images` — list images
- `docker rmi <image>` — remove image

## 2) Run containers
- `docker run <image>` — run container
- `docker run -it <image> bash` — interactive shell
- `docker run --rm <image>` — auto‑remove after exit
- `docker run -d --name <name> <image>` — background container
- `docker run -p 8080:80 <image>` — port mapping
- `docker run -v $PWD:/app <image>` — mount folder
- `docker run -e KEY=VALUE <image>` — env vars

## 3) Manage containers
- `docker ps` — running containers
- `docker ps -a` — all containers
- `docker stop <id>` — stop
- `docker rm <id>` — remove
- `docker logs -f <id>` — follow logs
- `docker exec -it <id> bash` — shell into container

## 4) Build images
- `docker build -t name:tag .` — build from Dockerfile
- `docker build --no-cache -t name:tag .` — clean build

## 5) Cleanup
- `docker system prune` — remove unused data
- `docker image prune -a` — remove unused images

## 6) Compose
- See `system/docker-compose.md` for compose workflows
