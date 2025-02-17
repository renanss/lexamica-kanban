# Lexamica Kanban

A modern Kanban board application with real-time updates and drag-and-drop functionality.

## Project Structure

This monorepo contains:
- Docker Compose configuration for local development
- Backend service (Node.js, Express, MongoDB)
- Frontend service (Next.js, React Bootstrap, WebSocket)

## Related Repositories

- [lexamica-kanban-frontend](https://github.com/renanss/lexamica-kanban-frontend) - Frontend application built with Next.js
- [lexamica-kanban-database](https://github.com/renanss/lexamica-kanban-database) - Database initialization and migrations

## Features

- Real-time updates using WebSocket
- Drag-and-drop task management
- Responsive design with Bootstrap
- RESTful API with MongoDB
- Docker containerization

## Quick Start

1. Clone the repositories:
```bash
mkdir lexamica && cd lexamica
git clone https://github.com/renanss/lexamica-kanban.git
git clone https://github.com/renanss/lexamica-kanban-frontend.git frontend
git clone https://github.com/renanss/lexamica-kanban-database.git database
```

2. Set up environment:
```bash
cp .env.example .env
```

3. Start services:
```bash
docker-compose up -d
```

The application will be available at:
- Frontend: http://localhost:3000
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
# MongoDB (use Docker service name for inter-container communication)
MONGODB_URL=mongodb://mongodb:27017/kanban
MONGO_INITDB_DATABASE=kanban

# Backend
BACKEND_PORT=4000
NODE_ENV=development

# Frontend (use Docker service name for inter-container communication)
NEXT_API_URL=http://backend:4000
```

Note: When running in Docker, use service names (e.g., 'mongodb', 'backend') instead of 'localhost' for inter-container communication.

## Contributing

Please refer to each project's style and contribution guidelines for submitting patches and additions. In general, we follow the "fork-and-pull" Git workflow.

## License

[MIT License](LICENSE) 