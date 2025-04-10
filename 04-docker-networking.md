# Day 4: Docker Networking — Container Communication

## Objective
Learn how to connect multiple containers together using a custom Docker network.

---

## ✅ Concepts Covered

- Docker networking types: `bridge`, `host`, `none`, `overlay`
- Creating a user-defined network
- Container name-based DNS resolution
- Testing communication using `curl`

---

## 🔧 Commands Used

### Create a Network
```bash
docker network create my-net


Run Nginx in Custom Network
docker run -d --name myweb --network my-net rakshit-nginx:v1


Run Alpine in Same Network and Test
docker run -it --name test-client --network my-net alpine
apk add curl
curl myweb

