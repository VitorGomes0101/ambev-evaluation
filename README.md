# Technical Evaluation Project

This repository contains the solution for a technical evaluation project. The application is built with a modern, multi-layered architecture and integrates various technologies to deliver a robust and scalable solution. Below, you'll find instructions to set up, run, and test the project locally.

---

## 🚀 Getting Started

Follow these steps to get the project up and running on your local machine.

### Prerequisites

Before you begin, ensure you have the following installed:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- [.NET SDK 8.0+](https://dotnet.microsoft.com/download)
- An IDE or code editor (e.g., [Visual Studio](https://visualstudio.microsoft.com/), [VS Code](https://code.visualstudio.com/))

---

## 🛠️ Project Architecture

The project is designed with a modular architecture and uses the following technologies:

- **Web API**: The core of the application, built with .NET 8.
- **PostgreSQL**: Primary relational database for structured data storage.
- **MongoDB**: NoSQL database for handling unstructured or semi-structured data.
- **Redis**: In-memory data store used for caching and improving performance.

---

## 🐳 Setting Up with Docker

To simplify the setup process, the project includes a `docker-compose.yml` file that configures and runs all required services.

### Steps to Run the Project

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/VitorGomes0101/ambev-evaluation.git
   cd ambev-evaluation
   ```
2. **Build and Run the Containers**:
   ```bash
   docker-compose up --build
   ```
   This command will:
   - Build the Docker image for the Web API.
    
   - Start all services defined in the docker-compose.yml file:
    
      - Web API: Accessible at http://localhost:8080 (HTTP) and https://localhost:8081 (HTTPS).
      
      - PostgreSQL: Available on port 5432.
      
      - MongoDB: Available on port 27017.
      
      - Redis: Available on port 6379.
        
3. **Verify the Services**:

    - Use docker ps to check if all containers are running.

    - Access the Web API endpoints via your browser or a tool like Postman.
    
---

🧪 Running Tests
The project includes unit and integration tests to ensure code quality and functionality. To run the tests, use the following command:

```bash
dotnet test
```
Make sure all services are running, as some tests may depend on the database or cache.

---

🛑 Stopping the Environment
To stop all running containers, use:
```
bash
docker-compose down
```
To remove unused containers, images, and volumes, run:
```
bash
docker system prune -a
```
         
