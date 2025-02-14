# Lexamica Kanban

A Kanban board application with a monolithic architecture.

## Repository Structure

This repository contains:

- Docker Compose configuration for local development
- Environment configuration templates
- Documentation for the overall system

## Related Repositories

- [lexamica-kanban-backend](https://github.com/renanss/lexamica-kanban-backend) - Main application service
- [lexamica-kanban-database](https://github.com/renanss/lexamica-kanban-database) - Database initialization and migrations

## Prerequisites

- Docker and Docker Compose
- Git

## Quick Start

1. Clone all required repositories:
```bash
# Create a directory for all repositories
mkdir lexamica && cd lexamica

# Clone repositories
git clone https://github.com/renanss/lexamica-kanban.git
git clone https://github.com/renanss/lexamica-kanban-backend.git backend
git clone https://github.com/renanss/lexamica-kanban-database.git database
```

2. Set up environment variables:
```bash
cp .env.example .env
```

3. Start the services:
```bash
docker-compose up -d
```

The services will be available at:
- Backend API: http://localhost:4000
- API Documentation: http://localhost:4000/api-docs

## Development Workflow

1. For frontend development:
   - Work in the frontend repository
   - Use the provided API endpoints from the backend service

2. For backend development:
   - Work in the backend repository
   - Use the provided database service

3. For database changes:
   - Work in the database repository
   - Test changes using the provided MongoDB service

## Environment Variables

The following environment variables can be configured in `.env`:

```env
# MongoDB
MONGODB_URL=mongodb://mongodb:27017/kanban
MONGO_INITDB_DATABASE=kanban

# Backend
BACKEND_PORT=4000
NODE_ENV=development

# Frontend (when implemented)
NEXT_PUBLIC_API_URL=http://localhost:4000
```

## Contributing

Please refer to each project's style and contribution guidelines for submitting patches and additions. In general, we follow the "fork-and-pull" Git workflow.

## License

[MIT License](LICENSE) 