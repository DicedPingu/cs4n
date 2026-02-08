# Docker - container engine and image runtime
# Use it to package apps as immutable images and run them consistently.

## Build-run-debug loop
- `docker build -t app:dev .` - build image from `Dockerfile`.
- `docker run --rm -it app:dev` - run interactive container.
- `docker run -d --name app -p 8080:8080 app:dev` - detached service container.
- `docker logs -f app` - stream logs.
- `docker exec -it app sh` - interactive shell inside container.

## Image and container management
- `docker images` - local images.
- `docker ps` / `docker ps -a` - running/all containers.
- `docker stop app && docker rm app` - stop and remove container.
- `docker rmi app:dev` - remove image.

## Volume, network, and env controls
- `docker run -v "$PWD":/workspace -w /workspace app:dev <cmd>` - bind mount workflow.
- `docker run --network host <image>` - host networking (Linux only, use intentionally).
- `docker run --env-file .env <image>` - inject environment variables.

## Cleanup without surprises
- `docker system df` - inspect resource usage first.
- `docker system prune` - remove stopped/unused resources.
- `docker image prune -a` - remove unused images.

## Version and release line
- Local check: `docker version`
- Upstream release snapshot: Docker Engine `docker-v29.2.1`.

