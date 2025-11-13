# Quick start
1. Create a `.env` file or set the environment variables: `DB_HOST`, `DB_USER`, `DB_PASSWORD`, `DB_NAME`, `DB_PORT`, `SERVER_PORT`
2. Build and run using `docker-compose`: 

```bash
docker-compose up
```

# Docker Build Optimization
The project uses Docker layer caching for faster rebuilds:
- Dependencies (go.mod/go.sum) are cached separately from source code
- `.dockerignore` excludes documentation, IDE configs, and other non-essential files
- Minor changes to docs, README, or .env files won't invalidate the build cache

# Docs
Swagger docs are available at /swagger