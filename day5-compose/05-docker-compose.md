# Day 5: Docker Compose - Multi-Container Mastery

Welcome to Day 5 of Rakshit's Docker journey, powered by ChatGPT!  
Today, we tackled **Docker Compose**, a tool to define and run multi-container applications using a single YAML file.

---

## What I Learned

- How to use `docker-compose.yml` to spin up multiple services.
- Shared network between containers using custom bridge network.
- How to mount a volume to Nginx using Compose.
- How to test internal container communication using Alpine + curl.
- How to start and stop everything in one command.

---

## Project Structure


day5-compose/ ├── docker-compose.yml └── nginx-html/ └── index.html


---

## docker-compose.yml

```yaml
version: '3'
services:
  web:
    image: nginx
    ports:
      - "8085:80"
    volumes:
      - ./nginx-html:/usr/share/nginx/html
    networks:
      - mynet

  client:
    image: alpine
    command: sh -c "apk add curl && sleep 3600"
    networks:
      - mynet

networks:
  mynet:
    driver: bridge




How to Run

# Step into the project directory
cd day5-compose

# Start services
docker-compose up -d

# Verify everything works
curl http://localhost:8085

# Enter client container
docker exec -it <client_container_id> sh
curl web   # This should return the HTML content

# Stop and clean up
docker-compose down
<h1>Hello from Rakshit - Compose Style!</h1>




Summary
Today I built a full two-service stack using Compose.
This is how real-world apps are deployed in microservices — and I took the first big step!

Tomorrow, we dive into Dockerfile + Compose combo — Dev environment style!
