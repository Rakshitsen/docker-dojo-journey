# Day 3: Docker Volumes — Data Persistence

## Objective
Learn how to persist data using Docker Volumes and demonstrate live editing with bind mounts.

---

## ✅ Concepts Covered

- Bind Mount vs Named Volume
- Using `-v` flag to mount files/folders
- How volumes help in persisting container data
- Real-time website updates using local file mapping

---

## 🔧 Commands Used

### Bind Mount (Live Edit)
```bash
mkdir docker-nginx-volume
cd docker-nginx-volume
echo "<h1>Hello from Volume!</h1>" > index.html

docker run -d -p 8082:80 -v $(pwd)/index.html:/usr/share/nginx/html/index.html nginx



Test Live Change

echo "<h1>Rakshit changed this LIVE!</h1>" > index.html

Named Volume Example

docker volume create myvol
docker run -d -p 8083:80 -v myvol:/usr/share/nginx/html nginx

