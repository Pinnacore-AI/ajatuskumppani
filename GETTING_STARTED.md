# Getting Started with Ajatuskumppani

Welcome to Ajatuskumppani! This guide will help you get started with the project, whether you're a developer, contributor, or just curious about the platform.

## Quick Start

### Prerequisites

Before you begin, ensure you have the following installed:

- **Docker & Docker Compose** (recommended for easiest setup)
- **Python 3.11+** (for backend development)
- **Node.js 18+** (for frontend development)
- **Git** (for version control)

### Option 1: Docker Compose (Recommended)

The fastest way to get started is using Docker Compose:

```bash
# Clone the main repository
git clone https://github.com/Pinnacore-AI/ajatuskumppani.git
cd ajatuskumppani

# Start all services
docker-compose up -d

# Check that services are running
docker-compose ps
```

This will start:
- PostgreSQL with pgvector extension
- Redis for caching
- AjatusServer API (http://localhost:8000)
- AjatusUI web interface (http://localhost:3000)

### Option 2: Manual Setup

If you prefer to run services individually:

#### 1. Set up AjatusServer (Backend)

```bash
# Clone the repository
git clone https://github.com/Pinnacore-AI/ajatus-server.git
cd ajatus-server

# Create virtual environment
python3.11 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set environment variables
export DATABASE_URL="postgresql://user:pass@localhost:5432/ajatus"
export REDIS_URL="redis://localhost:6379"
export SECRET_KEY="your-secret-key-here"

# Run the server
uvicorn api.main:app --reload
```

The API will be available at http://localhost:8000

#### 2. Set up AjatusCore (LLM)

```bash
# Clone the repository
git clone https://github.com/Pinnacore-AI/ajatus-core.git
cd ajatus-core

# Install dependencies
pip install -r requirements.txt

# Run inference (requires Ollama to be installed)
python inference/run.py --prompt "Hei, miten voin auttaa?"
```

#### 3. Set up AjatusUI (Frontend)

```bash
# Clone the repository
git clone https://github.com/Pinnacore-AI/ajatus-ui.git
cd ajatus-ui

# Install dependencies
yarn install

# Set API URL
export REACT_APP_API_URL="http://localhost:8000"

# Start development server
yarn start
```

The UI will be available at http://localhost:3000

## Development Workflow

### 1. Fork and Clone

```bash
# Fork the repository on GitHub, then clone your fork
git clone https://github.com/YOUR_USERNAME/ajatus-server.git
cd ajatus-server

# Add upstream remote
git remote add upstream https://github.com/Pinnacore-AI/ajatus-server.git
```

### 2. Create a Branch

```bash
# Create a new branch for your feature
git checkout -b feature/your-feature-name
```

### 3. Make Changes

Make your changes, following the coding standards:

- **Python**: Follow PEP 8, use `ruff` for linting
- **TypeScript**: Follow the existing code style, use ESLint
- **Commits**: Use [Conventional Commits](https://www.conventionalcommits.org/)

### 4. Test Your Changes

```bash
# Run tests
pytest tests/

# Run linting
ruff check .
```

### 5. Submit a Pull Request

```bash
# Push your changes
git push origin feature/your-feature-name

# Create a pull request on GitHub
```

## Project Structure

```
ajatuskumppani/
├── ajatus-core/        # LLM and inference engine
├── ajatus-server/      # Backend API
├── ajatus-node/        # Decentralized compute node
├── ajatus-ui/          # Frontend application
├── ajatus-memory/      # Vector memory system
├── ajatus-token/       # Blockchain token
└── ajatus-agents/      # Autonomous agents
```

## Common Tasks

### Running Tests

```bash
# Backend tests
cd ajatus-server
pytest tests/ -v

# Frontend tests
cd ajatus-ui
yarn test
```

### Building Docker Images

```bash
# Build server image
cd ajatus-server
docker build -t ajatus-server:latest .

# Build core image
cd ajatus-core
docker build -t ajatus-core:latest .
```

### Database Migrations

```bash
# Create a new migration
cd ajatus-server
alembic revision --autogenerate -m "Description"

# Apply migrations
alembic upgrade head
```

## Troubleshooting

### Port Already in Use

If you get a "port already in use" error:

```bash
# Find the process using the port
lsof -i :8000

# Kill the process
kill -9 <PID>
```

### Database Connection Issues

Ensure PostgreSQL is running and the connection string is correct:

```bash
# Check PostgreSQL status
systemctl status postgresql

# Test connection
psql -h localhost -U ajatus -d ajatuskumppani
```

### Docker Issues

```bash
# Remove all containers and volumes
docker-compose down -v

# Rebuild images
docker-compose build --no-cache

# Start fresh
docker-compose up -d
```

## Next Steps

- Read the [CONTRIBUTING.md](CONTRIBUTING.md) guide
- Check out the [ROADMAP.md](ROADMAP.md) to see what's coming
- Join our community on Discord (coming soon)
- Explore the [documentation](docs/)

## Getting Help

- **Telegram**: Join our community at https://t.me/ajatuskumppani
- **Issues**: Report bugs or request features on [GitHub Issues](https://github.com/Pinnacore-AI/ajatuskumppani/issues)
- **Discussions**: Ask questions on [GitHub Discussions](https://github.com/Pinnacore-AI/ajatuskumppani/discussions)
- **Email**: Contact us at ajatuskumppani@pinnacore.ai

---

**Built in Finland. Open to the world.** 🇫🇮

Welcome to The ThoughtMate Revolution!

