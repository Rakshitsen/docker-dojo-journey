# Basic Docker Commands (Single Container)

| Command | Description |
|---------|-------------|
| `docker pull <image>` | Download image from Docker Hub |
| `docker images` | List all downloaded images |
| `docker run <image>` | Run a container from an image |
| `docker run -d <image>` | Run container in detached mode (background) |
| `docker run -it <image> bash` | Run container with interactive terminal |
| `docker ps` | List running containers |
| `docker ps -a` | List all containers (running + stopped) |
| `docker stop <container_id>` | Stop a running container |
| `docker start <container_id>` | Start a stopped container |
| `docker restart <container_id>` | Restart a container |
| `docker rm <container_id>` | Remove a container |
| `docker rmi <image_id>` | Remove an image |
| `docker exec -it <container_id> bash` | Access running container terminal |
| `docker logs <container_id>` | View container logs |
| `docker build -t <tagname> .` | Build image from Dockerfile |



Docker compose

# Docker Compose Commands

(Used for multi-container setups using `docker-compose.yml`)

| Command                              | Description                                      |
|--------------------------------------|--------------------------------------------------|
| `docker-compose up`                 | Start all services in foreground                |
| `docker-compose up -d`              | Start all services in detached (background) mode|
| `docker-compose down`              | Stop and remove all services and networks       |
| `docker-compose build`             | Build images defined in the Compose file        |
| `docker-compose ps`                | List all running services                       |
| `docker-compose logs`              | Show logs of all services                       |
| `docker-compose exec <service> bash`| Open terminal in a running service              |
| `docker-compose restart`           | Restart all services                            |
| `docker-compose stop`              | Stop all services without removing them         |
| `docker-compose start`             | Start previously stopped services               |