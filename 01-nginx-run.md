# Day 1 - Running My First Docker Container

## What I Did:
- Installed Docker on my EC2 instance.
- Ran an nginx web server in a Docker container.
- Exposed the server on port 8080.
- Learned how Docker pulls images automatically.
- Customized the nginx homepage using bind mounts.

## Commands I Used:
- docker run -d -p 8080:80 nginx
- docker ps
- docker stop <container_id>
- docker rm <container_id>
- docker images

## What I Learned:
- Difference between image and container.
- What -p and -d flags do.
- How Docker pulls images automatically if not found locally.
- How to bind custom content into a container.





 docker run -d -p 8080:80 -v $(pwd)/nginx-html/:/usr/share/nginx/html nginx:latest
this command bothered me for while because i haven't study docker volume till now but i understand a bit how actually it works


![image](https://github.com/user-attachments/assets/a65a2cf0-85ea-4779-b30e-b8e1d60468c7)










1. Difference between Docker Image and Container:

Docker Image: A read-only blueprint (template) with everything your app needs—code, libraries, dependencies, OS files.

Container: A running instance of an image. Think of it as a live app launched from that blueprint.
Analogy: Image = recipe, Container = cooked dish from that recipe.

2. What does -p 8080:80 mean?

Docker containers (like nginx) expose their services on internal ports—nginx uses port 80.

-p 8080:80 tells Docker:
“Map my host machine’s port 8080 to the container’s port 80.”
So when you visit localhost:8080, Docker routes that to the container’s web server on port 80.


3. What does -d do?

-d stands for detached mode.

It runs the container in the background, letting you use the terminal freely.

Without -d, the container logs flood your terminal, and it blocks further commands.



4. Does deleting a container delete the image?

No, deleting a container does not delete its image.

The image stays unless you manually delete it with:

docker rmi <image_id>

5. Can two containers run from the same image?

Yes, you can run multiple containers from the same image.

They are isolated from each other and work independently—like launching multiple browser windows from the same installer.
   
