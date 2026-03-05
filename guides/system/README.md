# System Container Guides
Container image and multi-service stack workflows.

## Files and locations
- `guides/system/docker.md` - image, container, network, volume operations.
- `guides/system/docker-compose.md` - compose stack lifecycle and troubleshooting.

## Recommended order
1. `docker.md`
2. `docker-compose.md`

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `docker ps --format 'table {{.Names}}\t{{.Image}}\t{{.Status}}'` | Quick container status view |
| `docker images --digests` | Show local images with content digests |
| `docker run --rm -it alpine:latest sh` | Launch ephemeral shell container |
| `docker logs -f <container>` | Follow container logs live |
| `docker exec -it <container> sh` | Open shell inside running container |
| `docker build -t <name>:<tag> .` | Build image from current directory |
| `docker compose config` | Validate/render compose config |
| `docker compose up -d` | Start stack in background |
| `docker compose logs -f --tail=200` | Stream compose service logs |
| `docker compose exec <service> sh` | Run shell inside compose service |
| `docker compose down --remove-orphans` | Stop stack and clean orphan containers |
| `docker system df` | View Docker disk usage before cleanup |
