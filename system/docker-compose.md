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

