# Docker Compose - multi-container application orchestration
Use it to define app stacks (db, api, cache, workers) in one declarative file.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Daily stack control
- `docker compose up -d` - start services in background.
- `docker compose ps` - container state overview.
- `docker compose logs -f --tail=200` - live logs.
- `docker compose down` - stop and remove stack.

## Rebuild and update flows
- `docker compose up -d --build` - rebuild images then start.
- `docker compose pull && docker compose up -d` - refresh images and restart.
- `docker compose restart <service>` - bounce one service.

## Interactive debugging
- `docker compose exec <service> sh` - shell inside service.
- `docker compose run --rm <service> <cmd>` - one-off command in service image.
- `docker compose config` - render merged/validated config.

## Environment and profile options
- `docker compose --profile dev up -d` - profile-specific services.
- `docker compose --env-file .env.local up -d` - custom env file.

## Version and release line
- Local check: `docker compose version`
- Upstream release snapshot: Docker Compose `v5.0.2`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `docker compose ps` | List all running containers |
| `docker compose up [-d\|--detach]` | Create and start all containers in the background using a `docker-compose.yml` file from the current directory |
| `docker compose up --build` | Start all containers, rebuild if necessary |
| `docker compose [-p\|--project-name] project_name [-f\|--file] path/to/file up` | Start all containers by specifying a project name and using an alternate compose file |
| `docker compose stop` | Stop all running containers |
| `docker compose down --rmi all [-v\|--volumes]` | Stop and remove all containers, networks, images, and volumes |
| `docker compose logs [-f\|--follow]` | Follow logs for all containers |
| `docker compose logs [-f\|--follow] container_name` | Follow logs for a specific container |
| `docker-compose --help` | Show command usage and option reference |
| `man docker-compose` | Open the full manual page |
| `whatis docker-compose` | Print one-line command description |
| `type -a docker-compose` | Show how the shell resolves the command path |
| `command -v docker-compose` | Print executable path used by current shell |
| `tldr docker-compose` | Show concise command examples |
| `apropos docker-compose` | Search manual database for related commands |
| `docker-compose --version` | Print local tool version |
| `docker ps [-a\|--all]` | List all Docker containers (running and stopped) |
| `docker run --name container_name image` | Start a container from an image, with a custom name |
| `docker start\|stop container_name` | Start or stop an existing container |
| `docker pull image` | Pull an image from a Docker registry |
