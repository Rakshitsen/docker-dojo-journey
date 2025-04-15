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

Used for multi-container setups using docker-compose.yml)
CommandDescriptiondocker-compose upStart all services in foregrounddocker-compose up -dStart all services in detached (background) modedocker-compose downStop and remove all services and networksdocker-compose buildBuild images defined in the Compose filedocker-compose psList all running servicesdocker-compose logsShow logs of all servicesdocker-compose exec <service> bashOpen terminal in a running servicedocker-compose restartRestart all servicesdocker-compose stopStop all services without removing themdocker-compose startStart previously stopped services
