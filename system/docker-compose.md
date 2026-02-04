# Docker Compose — multi‑container workflows
# Use it to define and run multi‑service apps.

## Basics
- `docker compose up -d` — start services
- `docker compose down` — stop + remove
- `docker compose ps` — list containers
- `docker compose logs -f` — follow logs

## Useful options
- `docker compose up --build -d` — rebuild then start
- `docker compose exec <svc> bash` — shell in service
- `docker compose restart <svc>` — restart one service
