FROM bigcapitalhq/server:latest

# Run migrations as the non-root user from the server image. Compose waits for
# MariaDB health before starting this one-shot service.
WORKDIR /app/packages/server

CMD ["sh", "-c", "node dist/cli.js system:migrate:latest && node dist/cli.js tenants:migrate:latest"]
