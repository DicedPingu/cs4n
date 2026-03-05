# Docker - container engine and image runtime
Use it to package apps as immutable images and run them consistently.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

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

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `docker ps [-a\|--all]` | List all Docker containers (running and stopped) |
| `docker run --name container_name image` | Start a container from an image, with a custom name |
| `docker start\|stop container_name` | Start or stop an existing container |
| `docker pull image` | Pull an image from a Docker registry |
| `docker images` | Display the list of already downloaded images |
| `docker exec [-it\|--interactive --tty] container_name sh` | Open an interactive tty with Bourne shell (`sh`) inside a running container |
| `docker rm container1 container2 ...` | Remove stopped containers |
| `docker logs [-f\|--follow] container_name` | Fetch and follow the logs of a container |
| `docker --help` | Show command usage and option reference |
| `man docker` | Open the full manual page |
| `whatis docker` | Print one-line command description |
| `type -a docker` | Show how the shell resolves the command path |
| `command -v docker` | Print executable path used by current shell |
| `tldr docker` | Show concise command examples |
| `apropos docker` | Search manual database for related commands |
| `docker --version` | Print local tool version |
