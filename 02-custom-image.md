# Day 2: Custom Docker Image with Nginx

## Objective
Create a Docker image using a custom HTML page served by Nginx.

---

## Steps Followed:

1. **Created project folder**
```bash
mkdir docker-custom-nginx
cd docker-custom-nginx

#Created a custom HTML page
echo "<h1>This is Rakshit's Custom Nginx Image!</h1>" > index.html

#Wrote Dockerfile
FROM nginx
COPY index.html /usr/share/nginx/html

#Built Docker image
docker build -t rakshit-nginx:v1 .

#Ran container
docker run -d -p 8080:80 rakshit-nginx:v1

#Checked result in browser
![Screenshot 2025-04-09 195936](https://github.com/user-attachments/assets/955c3466-0c30-4b0f-bb40-a28e12011a57)

