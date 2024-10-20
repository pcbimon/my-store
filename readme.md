# MedusaJS Store in Docker Compose
## Instruction
1. Copy Backend and Frontend to the same directory
2. Run `docker-compose up -d`

## Backup and Restore Database
1. Backup
```bash
docker exec -t app-db pg_dumpall -c -U medusauser > dump_YYYYMMDD.sql
```
2. Restore
```bash
docker compose exec db psql -U medusauser -d medusadb -f /tmp/backup/dump_YYYYMMDD.sql
```
# Admin Password
admin@medusa-test.com
medusastore_itds362