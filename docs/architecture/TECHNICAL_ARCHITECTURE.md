_# Ajatuskumppani - Technical Architecture

This document provides a detailed overview of the technical architecture of the Ajatuskumppani project.

## System Overview

The system is designed as a modular, microservice-based architecture. The core components are:

-   **AjatusUI**: The user-facing application.
-   **AjatusServer**: The central backend service.
-   **AjatusCore**: The AI model and inference engine.
-   **AjatusMemory**: The long-term memory and user profile service.
-   **AjatusNode**: The decentralized compute nodes.
-   **AjatusAgents**: Autonomous agents for specific tasks.
-   **AjatusToken**: The blockchain-based token.

![System Architecture](/home/ubuntu/ajatuskumppani/docs/architecture/system_architecture.png)

## Component Details

### AjatusServer (FastAPI)

-   **Authentication**: JWT-based authentication with access and refresh tokens.
-   **API**: RESTful API for all standard operations. WebSockets for real-time communication with AjatusUI.
-   **Database**: PostgreSQL with `pgvector` for structured data and vector embeddings. SQLAlchemy as the ORM.
-   **Caching**: Redis for caching frequently accessed data and for message queuing.
-   **Task Orchestration**: Celery for background tasks and for orchestrating the AjatusAgents.

### AjatusCore (Python)

-   **Model**: Fine-tuned version of Mistral 7B Instruct.
-   **Inference**: vLLM for high-throughput serving on GPUs. Ollama as a fallback and for CPU-based inference.
-   **API**: A simple internal API for the AjatusServer to get model completions.

### AjatusMemory (Python)

-   **Embedding Generation**: Uses `sentence-transformers` to generate embeddings for user interactions.
-   **Vector Storage**: `pgvector` for storing and querying embeddings. FAISS for in-memory indexing and faster retrieval.
-   **User Profile**: A service that continuously updates a user's profile based on their interactions and retrieved memories.

### AjatusNode (Python/Docker)

-   **Compute Environment**: Docker containers for securely and isolating AI tasks.
-   **Proof-of-Contribution**: A custom algorithm that measures uptime, performance, and task validation to reward nodes.
-   **Networking**: A P2P network for communication between nodes.

### AjatusUI (React Native)

-   **State Management**: Zustand for simple and scalable state management.
-   **API Communication**: Axios for REST API calls and the native WebSocket API for real-time updates.
-   **Styling**: Tailwind CSS for a consistent and modern look and feel.

### AjatusToken (Solidity)

-   **Contract**: An ERC-20 compliant token contract.
-   **Staking**: A staking contract that allows users to lock up their tokens and earn rewards.
-   **Governance**: A governance contract that allows token holders to vote on proposals.

## Data Flow

1.  A user interacts with the **AjatusUI**.
2.  The UI sends a request to the **AjatusServer**.
3.  The server authenticates the user and processes the request.
4.  If the request requires AI completion, the server sends a prompt to the **AjatusCore**.
5.  The **AjatusCore** returns the completion to the server.
6.  The server stores the interaction and its embedding in the **AjatusMemory**.
7.  The server returns the response to the UI.

## Security

-   All communication between services is encrypted with TLS.
-   User data is encrypted at rest.
-   The AjatusNode uses Docker containers to isolate tasks and prevent malicious code from accessing the host system.
-   Regular security audits will be performed.

