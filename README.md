# Docker Compose UI Demo

A comprehensive Docker Compose demo application with a modern UI for presentations and learning purposes. This project demonstrates a full-stack application architecture using Docker Compose to orchestrate multiple services.

## Architecture

This demo consists of three main components:

1. **Frontend**: A React application with a modern UI for task management
2. **Backend**: A Node.js Express API that handles task data
3. **Database**: A PostgreSQL database for persistent storage

The services are connected through a Docker network, demonstrating container networking concepts.

## Features

- Full CRUD operations for managing tasks
- Clean, responsive UI with Bootstrap
- Proper service separation and communication
- Database persistence with volume mapping
- Easy deployment with a single command

## Prerequisites

- Docker (20.10+)
- Docker Compose (2.0+)

## Running the Demo

1. Clone this repository:
   ```bash
   git clone https://github.com/ajeetraina/docker-compose-ui-demo.git
   cd docker-compose-ui-demo
   ```

2. Start the application with Docker Compose:
   ```bash
   docker-compose up -d
   ```

3. Access the application:
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:5000
   - Database: localhost:5432 (PostgreSQL)

4. To stop the application:
   ```bash
   docker-compose down
   ```

## Key Concepts Demonstrated

- **Service Orchestration**: Using Docker Compose to define and run multi-container applications
- **Container Networking**: Services communicate with each other through a Docker bridge network
- **Data Persistence**: Using Docker volumes for database persistence
- **Environment Configuration**: Using environment variables for service configuration
- **Multi-stage Builds**: Optimizing container size and security (frontend Dockerfile)
- **API Communication**: Frontend to backend communication via RESTful API

## Project Structure

```
docker-compose-ui-demo/
├── docker-compose.yml       # Main docker-compose configuration
├── frontend/                # React frontend application
│   ├── Dockerfile
│   ├── nginx.conf
│   ├── package.json
│   └── src/
│       ├── App.js
│       └── ...
├── backend/                 # Node.js backend API
│   ├── Dockerfile
│   ├── package.json
│   └── server.js
└── db/                      # Database initialization
    └── init/
        └── init.sql
```

## Extending the Demo

Here are some ways you can extend this demo:

1. Add user authentication
2. Implement real-time updates with WebSockets
3. Add a Redis service for caching
4. Deploy with Docker Swarm or Kubernetes
5. Add monitoring with Prometheus and Grafana

## Troubleshooting

**Issue**: Frontend can't connect to the backend
- Solution: Check that the backend service is running with `docker-compose ps`
- Verify network configuration in `docker-compose.yml`

**Issue**: Database connection issues
- Solution: Check the environment variables in the backend service
- Ensure the database initialization script runs correctly

## License

MIT

---

Happy Docker Composing! 🐳