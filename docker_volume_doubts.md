A Docker volume is a persistent storage mechanism used to store data independently of a container's lifecycle. It helps retain data even after the container is stopped or removed.


Difference between Docker volumes and bind mounts?
Volume is managed by Docker ( docker volume) and stored in Docker's storage area.

Bind mount directly maps a host path to the container.

Volumes are preferred for portability and ease of backup.



3.How do you create and use a Docker volume?
# Create a named volume
docker volume create my_volume

# Use it in a container
docker run -d -v my_volume:/app/data my_image


4.Where are volumes stored on the host?
Volumes are stored in /var/lib/docker/volumes/on Linux-based systems.

5. What happens to a volume when a container is removed?
Answer:
The volume persists unless you explicitly remove it with docker volume rm.


 6. How to share data between containers?
    # Run first container with a volume
    docker run -d --name container1 -v shared_volume:/app/data busybox

    # Run second container with the same volume
    docker run -d --name container2 -v shared_volume:/app/data busybox


 7. Inspect volume content?
   # Use a temporary container to explore the volume
  docker run --rm -it -v my_volume:/data busybox sh
  # Inside the container: `ls /data`
