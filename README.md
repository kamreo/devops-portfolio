# multi-sevice-app
 
This project is a fully containerized web application using .NET Core for the API, React for the frontend, PostgreSQL for the database, Nginx as a reverse proxy, and Redis for caching.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Docker and Docker Compose are installed on your system.
- Basic knowledge of .NET Core, React, PostgreSQL, Nginx, and Docker.

## Project Structure

- `api/`: Contains the .NET Core Web API project.
- `frontend/`: Contains the React application.
- `nginx/`: Contains the Nginx configuration files.
- `docker-compose.yml`: Defines the services, networks, and volumes for the application stack.

## Setup and Running

1. **Clone the repository:**
   ```bash
   git clone git@github.com:kamreo/devops-portfolio.git
   cd devops-portfolio
   ```

2. Build and run the Docker containers:

```
docker-compose up --build
```

3. Accessing the application:

- The React frontend will be available at http://localhost:3000.
- The .NET API will be accessible through the Nginx reverse proxy at http://localhost/api.